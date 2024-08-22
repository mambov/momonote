Watch this and send me an email describing what they were trying to do for an extra 10 points on your lowest grade. 
https://www.youtube.com/watch?v=mK3CLAXpL6s 


The Pied Piper team needs 120,000 phones to download their app.  
The public WiFi at the tech conventions requires that the user first downloads the HooliCon app. Their goal is, after they've hacked their code onto the app, to push it over the venue's free WiFi to unsuspecting users by launching a man in the middle attack with pineapples. A Wi-Fi pineapple is a device that allows attackers to intercept messages between a router and a device, with neither of them knowing of the attacker[1].

The team deploys the pineapples in high traffic areas. The reason for this is not only to get the most amount of users, but because the signal from the pineapple to the user needs to be as strong as possible. Specifically, the signal needs to be stronger from the pineapple than from the real WiFi router. Normally, this is because the phone automatically connects to the stronger connection after it has become trusted. It's important that the hacked version of the HooliCon app is downloaded before the legitimate one, as users probably won't be able to download both. There wouldn't be any second chance.

The pineapple can put itself "in the middle". The pineapple, perhaps using PineAP[2] or Kali Linux tools, is able to inspect the list of connected devices from the router. The pineapple is able to then pretend to be the connected device and intercept traffic. The pineapple is able to trick the phone in the same way. It pretends to be the legitimate router that it has or would have trusted and and is even able to pass through legitimate incoming traffic to the phone. But it is also able to choose when to respond with the malicious traffic.

In this example, when the WiFi requires the user to download the HooliCon app, the pineapple will instead redirect the user to install the hacked HooliCon app. The team's mission is then successful and the user is none the wiser. 

References:
[1] https://www.techtarget.com/searchsecurity/definition/Wi-Fi-Pineapple
[2] https://www.youtube.com/watch?v=mK3CLAXpL6s
