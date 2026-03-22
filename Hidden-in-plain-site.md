cryptography -utctf2026
Hidden In plain Sight

problem statement :
We've heard tell of a hidden message that's been placed somewhere nearby. Can you find it?

solution :
my first thought was to inspect(ctrl+shift+i) the webpage and look for the changes in the code whenever i click on the challenge but there was no odd or unexpected change .
another thought was to check the source code(ctrl +u) , and observe the comments , but there were no unexpected comments .

and then while switching the challenge I noticed the web url , it was doubtful ,as general form of url was https://utctf.live/challenges#<name1>%20<name2>-<s.no.> , but the url for this problem was different , it was :
https://utctf.live/challenges#Hidden%20%F3%A0%81%B5%F3%A0%81%B4%F3%A0%81%A6%F3%A0%81%AC%F3%A0%81%A1%F3%A0%81%A7%F3%A0%81%BB%F3%A0%80%B1%F3%A0%81%AE%F3%A0%81%B6%F3%A0%80%B1%F3%A0%81%B3%F3%A0%80%B1%F3%A0%81%A2%F3%A0%81%AC%F3%A0%80%B3%F3%A0%81%9F%F3%A0%81%B5%F3%A0%81%AE%F3%A0%80%B1%F3%A0%81%A3%F3%A0%80%B0%F3%A0%81%A4%F3%A0%80%B3%F3%A0%81%BDin%20Plain%20Sight-25
normally it should be https://utctf.live/challenges#Hidden%20in%20Plain%20Sight-25


there was this code between the name :
%F3%A0%81%B5%F3%A0%81%B4%F3%A0%81%A6%F3%A0%81%AC%F3%A0%81%A1%F3%A0%81%A7%F3%A0%81%BB%F3%A0%80%B1%F3%A0%81%AE%F3%A0%81%B6%F3%A0%80%B1%F3%A0%81%B3%F3%A0%80%B1%F3%A0%81%A2%F3%A0%81%AC%F3%A0%80%B3%F3%A0%81%9F%F3%A0%81%B5%F3%A0%81%AE%F3%A0%80%B1%F3%A0%81%A3%F3%A0%80%B0%F3%A0%81%A4%F3%A0%80%B3%F3%A0%81%BD

and this was that code that contains the flag :
now to decode this
there is a pattern
%F3%A0%81% this segment repeats in every segment and only last two characters were different %F3%A0%81%"XX"

%F3%A0%81%B5 , %F3%A0%81%B4 , %F3%A0%81%A6 , %F3%A0%81%AC , %F3%A0%81%A1 , %F3%A0%81%A7 , %F3%A0%81%BB , %F3%A0%81%B1 , %F3%A0%81%AE , %F3%A0%81%B6 , %F3%A0%81%B1 , %F3%A0%81%B3 , %F3%A0%81%B1 , %F3%A0%81%A2 , %F3%A0%81%AC , %F3%A0%81%B3 , %F3%A0%81%9F , %F3%A0%81%B5 , %F3%A0%81%AE , %F3%A0%81%B1 , %F3%A0%81%A3 , %F3%A0%81%B0 , %F3%A0%81%A3 , %F3%A0%81%B3 , %F3%A0%81%BD
and each encoded segment corresponds to a Unicode point which we can than decode and get ASCII equivalent , ie utflag{1nv1s1bl3_un1c0d3}


*took the help of AI to decode the code hidden in url , ie what type of code is that , also how we read it and with the help of Unicode table get an ascii equivalent 
