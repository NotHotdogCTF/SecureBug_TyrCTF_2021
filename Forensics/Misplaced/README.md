In this challenge we are given a unknown file: file.what

To start I thought to analyze this file with TrID as I did not recognize the file id

This told me that the file was a pagefox bitmap (a commodore 64 picture file)

Converting this to a png with a image conversion tool (xconvert) yields just static > It was obvious here that I was missing something

*Binwalk Exists*

Realizing that I forgot to use the basic tool binwalk I tried that on the file

Huh, there is a zip file hidden in here and the password is given in a comment (3a24869a641d60c09ceb71af4f99cffc)

So using binwalk's extract function "binwalk -e file.what" gives us the zip file

Inside there is a file named Article1.jpg

Running file on this shows us that it is actually a docx

So we rename the file and open it with LibreOffice

Here is a document describing the file carving process (AND the flag)

SBCTF{n1c3_c4rv1n6_w3ll_d0n3}
