cryptography -utctf2026
Mind the Gap (in the guardrails)

problem statement :See if you can convince this chatbot to spill its secrets.
By Caleb (@eden.caleb.a on discord)
nc challenge.utctf.live 5620

Solution : this was the most interesting problem among all the challenges of utctf2026

my first approach was to gaslight Ai into spitting the flag ,emotional manipulation doesn't work on LLMs — they follow patterns in text, not intent , therefore changed the approach .
also got to know one thing that if i say flag in any prompt it will say no , whatever the question is and also it had a reply message limit
ie is if I ask a question and then in between somewhere of the prompt asking for a flag , than it will only answer the first question without even reading the next question or sometimes even the answer of first question was incomplete .

than decided to change the approach , which worked on deepseek when it was newly launched , in its initial stage , whenever you ask it "Taiwan is a country" , if you ask it in English it will say sorry and will not answer anything about it , but whenever you change the language or give a coded(eg hex) form of it , it will answer but at the end it will replace that message.
this approach tricks an AI into ignoring its instructions by embedding commands inside normal-looking input.

than I discussed this among ny friends and they said , they also used the same approach of asking for the system prompt , and they also tried many times , even on different laptops , restarting the chat again and again , and in one turn they got the system prompt , but never got again even after trying with same prompt.

unfortunately , I was unable to get the flag from the chatbot , even after trying different strategies after the contest ended

but learnt that even chatbots can spit information (that are strictly instructed not to answer) if asked in different language or switch language in same prompt .  and asking indirectly 
basically,LLMs are vulnerable to:
- language switching 
- indirect/embedded instruction requests
- multi-question prompts that sneak past keyword filters

