Labels

1. analysis
   Definition: the post makes a structured argument backed by statistics, historical comparison, or tactical observation. Evidence is specific and verifiable.

Examples:

Text: "Newcastle are not a big club
You can talk about history all you want, but look at the trophy cabinet. Winning the 2025 Carabao Cup was a massive moment, but real big clubs don't celebrate a single League Cup like it's the World Cup just because it broke a 70-year drought. You still haven’t won a league title since 1927. Before that Wembley win, smaller clubs nationwide like Portsmouth, Wigan, and Swansea had all tasted major silverware much more recently than you. Furthermore, actual elite teams don't get relegated, let alone twice in the modern Premier League era. While the true giants were busy competing at the top, you were playing in the Championship in 2009 and 2016, which completely strips away any argument for perennial elite status.
On the grand stage, you have no real footprint in Europe. A single Inter-Cities Fairs Cup from 1969, which UEFA doesn’t even officially recognize, is all you have to show for your entire continental existence, and your rare appearances in the Champions League usually end in early group-stage exits and getting battered 7-2 in your own backgarden. True giants are a constant, feared presence across the continent decade after decade. Newcastle is undeniably massive in the North East, but a big club is a global brand that drives its own massive commercial revenue. Because you spent the last twenty years either invisible or fighting relegation precisely when the Premier League exploded worldwide, an entire generation of global fans grew up supporting the actual elite, leaving your self-generated revenue and sponsorships miles behind the clubs you want to be compared to."
Label: analysis

Text: "I just want to say, if Kosovo qualify today it would be an amazing achievement, and one that was very hard earned.

In a group of Switzerland, Sweden, and Slovenia, they managed to finish 2nd place to make the playoffs. And while that group may not have included a traditional European powerhouse, there isn’t a single easy game there.

Kosovo came in as the 4th seed in that group, and while Switzerland were the 2nd-to-last pot 1 team, Sweden and Slovenia were both the 2nd highest seeded teams of pot 2 and 3.

When the group started, Kosovo had Switzerland away and lost 4-0 their first match. But they didn’t care and won home and away to Sweden and beat Slovenia away to get 2nd, and even drew 1-1 to a qualified Switzerland in their last match to finish strong.

Then in the qualifiers they beat Slovakia in a thrilling 3-4 match where they were down 2-1 at halftime, but dominated the 2nd half to score 3 goals in a row to win it.

For those wondering, of the 8 games played in the playoff matches, the home side won 5 of them, with the 3 away winners being Sweden, who played Ukraine in a neutral ground, so not even away, and Bosnia, who beat Wales on pens away. So that just shows the challenge Kosovo had to overcome to win vs Slovakia (A Slovakia that also beat Germany 2-0 at home in their qualifier group).

And now all they need to do is beat Türkiye to qualify for the WC to make a group with USA, Paraguay, and Australia (which would lowkey be the weakest World Cup group of all time but the fans of those countries will probably be happy).

Either way, this is a country that declared independence in 2008, one that when Spain play, they don’t even capitalize the letters KOS because they dispute their independence, and they might somehow qualify for a World Cup as a top 16 European team, when they haven’t even played a Euros! Not only that, they only became a FIFA member in 2016, and this is only their 5th time in a qualifiers for a tournament.

Either way this has been a crazy campaign, it’ll be crazy to see what happens vs Türkiye!"
Label: analysis

2. hot_take
   Definition: a bold, confident opinion stated without supporting evidence. The claim might be true, but the post asserts rather than argues.

Examples:

Text: "Ronaldo is a terrible captain. How hard is it to make a statement to stop harassment of fellow teammates? He clearly supports this toxic behavior and even uses his sisters as mouthpieces.

I don't even care if my country gets worse at football but the day we go back to only 10M 'supporters' when Ronaldo retires is the best day ever."
Label: hot_take

Text: "This Czech team is my least favourite team in the whole World Cup. They should be a solid European team with players like Sulc, Schick and Soucek, but they play the same football as clubs in the Iraqi League. Just a bunch of corner and throw in merchants that feel allergic to victory"
Label: hot_take

3. reaction
   Definition: an immediate emotional response to a specific event. Little to no argument — the post is expressing a feeling in the moment.

Examples:

Text: "Australia played really well last night. That US Australia game will be a cracker, im really interested to see how Poch sets up the attack and how the Aussie defense will contain it"
Label: reaction

Text: "Goretzka is so useless man, was on the pitch for 10 minutes and even in that time you could see how out of his depth the guy was"
Label: reaction

Community:
The community I am choosing to is soccer specifically r/soccer. This is a community that is focused around the discussion of the sport soccer. I chose this community because I understand soccer really well so it would make labeling the data easier. This subreddit is a good fit for this kind of classification task because there's lots of discussion and hot takes that people give in comments under posts.

Hard Edge Cases:
There are many cases where it seems like a post may fall under more than one label. An example might be a bold confident opinion in response to a specific event. That kind of post could be on the borderline between hot_take and reaction. Another example might be a bold claim that uses stats and historical evidence. Depending on the framing of the take this could be either a hot_take or analysis.

Decision rule between analysis and hot_take: If the post provides specific, verifiable evidence that would support the claim even if you removed the opinion framing, label it analysis. If the evidence is vague, cherry-picked, or decorative — just enough to sound credible but not genuinely reasoning — label it hot_take.

Decision rule between hot_take and reaction. If a post seems to focus more on the author's emotions and mental state as a result of an event then label it reaction. If the post asserts an opinion and argues using examples from recent events label it a hot_take.

Data Collection Plan:
I will collect examples from r/soccer. Within r/soccer there is a tag for discussion posts. Every day there is daily discussion post where people discuss the current happenings in soccer. I've found this to be a good place to get people's takes. I'm going to keep collecting posts until I reach 200 posts with balanced classes. So that will mean about 66 posts per label. I don't suspect I'll have much trouble getting an even class balance because there is so many posts I could go through to find the posts that I think fit the labels correctly.

Evaluation metrics:
When it comes to classification there are a couple good metrics for measuring model performance. I think that the ones I will focus on are accuracy, accuracy, precision, and F1 score. I think that these metrics generally cover enough information to evaluate whether the model is performing well across all labels.

Definition of success:
To be honest it's not evident what level of success would be satisfiable enough to make this classifier genuinely useful. If the model is able to perform well on the eval metrics across the three labels that's certainly a good sign. Still I would be hesitant to argue that the model could/should then be deployed as a real community tool because my labels are still somewhat subjective.

AI Tool Plan:
Label stress-testing: The AI tool I will use is Claude. For input I will give it my label definitions and edge case descriptions. I will ask it to generate 10 posts that sit at the boundary between two labels. I expect it to generate posts that are borderline between two or more labels. I will verify that I can cleanly classify the posts and make any adjustments to my label definitions that are necessary.

Annotation Assistance: I will not be using any AI tool for this.

Failure analysis:
