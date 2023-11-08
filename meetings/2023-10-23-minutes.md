### Notes

1. [#236](https://github.com/patcg-individual-drafts/topics/issues/236) V2 taxonomy ramp up. (Leeron Israel)
    1. Currently at 10% on Stable, monitoring metrics
    2. There is no ID collison, since v2 includes new IDs, and the response also has the version IDs
    3. In about two weeks time, we will ramp to 100%
2. Understanding industry debugging needs. (Leeron Israel)
    4. There are many reasons why we may not be able to return a call, including, Per caller filter, options set by users, regulatory reasons and so on. 
    5. Are there other concerns from this group? 
    6. [Sid Sahoo] Local dev testing vs prod monitoring?
        1. [Leeron] - In production
    7. [Josh Karlin] - We have had some feedback for all the Privacy Sandbox APIs. 
        2. Topics and ARA don’t necessarily inform when it is going to fail or not respond with a topic (Topics API) and fail to convert (ARA)
        3. Feedback: For debugging, it may be useful to get a response of some kind. 
        4. It won’t change anything regarding  if you would get a topic or not,  but may help with debugging
        5. Will see if there is a github based PR or issue and respond accordingly. 
3. [#92](https://github.com/patcg-individual-drafts/topics/issues/92) Update permissions policy to support separate permissions for retrieve and observe
    8. [Leeron] Included the feature mainly from adtech feedback and regulatory reasons. Ability to read is the incentive.
    9. [Don Marti] Original implementation is similar to quid-pro-quo. To read a topic you should be contributing to topics by writing to it.
    10. [Don Marti] Example: NFL streams via smaller infringing sites seems to be well classified by Topics API, but larger streamers such as Amazon, etc. use NFL games to attract users to general content sites.  A dishonest SSP using small pirate sites can get better monetization, but the legit publishers can’t get much out of the API. Lot of these smaller sites also use deceptive practices (show google ads, and ask if you want to install a malware “ad blocker” extension). 
    11. [Don Marti] Does the Topics API incentivize harmful practices, by enabling these types of SSPs? (such as malware browser extensions used to drive traffic)
    12. [Josh Karlin] Is the concern about SSPs being able to retrieve the topics, without contributing to observed topics? 
    13. [Kleber] This view is dependent on if Topics API can distinguish between users in sketchy sites, and the authorized sites? 
    14. [Don Marti] Sets of topics are interpreted by ML on the caller side which assigns users to more or less valuable cohorts https://github.com/patcg-individual-drafts/topics/issues/221 
    15. [Josh Karlin] It is possible to see the imbalance, but not sure about the impact and there is a chance that limiting this may break the api. 
    16. [Don Marti] It is possible that some of these can be addressed at the attestation level, but right now the implementation incentivizes SSP behavior that is harmful to users. https://github.com/patcg-individual-drafts/topics/issues/266 
    17. [Josh Karlin] This seems like a much larger ecosystem level problem than what Topics API can cover on its own. We could be taking on more than what can be done via Topics API. 
    18. [Don Marti]  Browser code level is not the only level at which this problem can be addressed. Topics API is part of a market design that currently incentivizes user-harmful practices by third parties, and would need to be balanced in order to avoid having a net negative effect.

### Attendees: please sign yourself in!

1. Leeron Israel (Google Chrome)
2. Don Marti (Raptive)
3. Alex Cone (Google Privacy Sandbox)
4. Josh Karlin (Google Chrome) 
5. Sathish Manickam (Google Chrome)
6. Sid Sahoo (Google Chrome)
7. Alexandre Nderagakura (Not affiliated)
8. Yuyan Lei (Washington Post)
9. Achim Schlosser (European netID Foundation)
10. Michael Kleber (Google Privacy Sandbox)
