cryptography -utctf2026
Double Check 

problem statement :
We're planning on deploying some new static sites for our officers. We've cloned a template from Hugo's Static Site Generator (SSG). Can you make sure that our website is clean before it's deployed?

https://github.com/Jarpiano/utctf-profile

solution :
first i thought their would be some note or odd visible thing hiding somewhere in the website, looked everywhere but nowhere to be found , 
than i read the question again , they simply want me to find any sensitive information in the website hiding somewhere , than i thought that the UTCTF started very recently and they would have made the changes according to the ctf recently . AND GitHub always keeps the track of changes ie history , AND history appears in the commit section , therefore flag should be there in coded form or just in simple flag form 

and yes there were changes made in the website recently 
three commits were made recently on the same day and there was this flag
utflag{n07h1n6_70_h1d3}

learning : 
Never commit secrets , codes , important information,etc  to Git — even if you delete them immediately,
When you delete a file in Git and commit, the file looks gone but is permanently preserved in commit history. This is called Git Forensics or Secret Leakage via Git History.
