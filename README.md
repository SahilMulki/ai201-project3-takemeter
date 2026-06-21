# ai201-project3-takemeter

## Community

The community I am choosing to is soccer specifically r/soccer. This is a community that is focused around the discussion of the sport soccer. I chose this community because I understand soccer really well so it would make labeling the data easier. This subreddit is a good fit for this kind of classification task because there's lots of discussion and hot takes that people give in comments under posts.

## Label Taxonomy

### 1. analysis

**Definition:** The post makes a structured argument backed by statistics, historical comparison, or tactical observation. Evidence is specific and verifiable.

**Examples:**

> "Newcastle are not a big club
> You can talk about history all you want, but look at the trophy cabinet. Winning the 2025 Carabao Cup was a massive moment, but real big clubs don't celebrate a single League Cup like it's the World Cup just because it broke a 70-year drought. You still haven't won a league title since 1927. Before that Wembley win, smaller clubs nationwide like Portsmouth, Wigan, and Swansea had all tasted major silverware much more recently than you. Furthermore, actual elite teams don't get relegated, let alone twice in the modern Premier League era. While the true giants were busy competing at the top, you were playing in the Championship in 2009 and 2016, which completely strips away any argument for perennial elite status.
> On the grand stage, you have no real footprint in Europe. A single Inter-Cities Fairs Cup from 1969, which UEFA doesn't even officially recognize, is all you have to show for your entire continental existence, and your rare appearances in the Champions League usually end in early group-stage exits and getting battered 7-2 in your own backgarden. True giants are a constant, feared presence across the continent decade after decade. Newcastle is undeniably massive in the North East, but a big club is a global brand that drives its own massive commercial revenue. Because you spent the last twenty years either invisible or fighting relegation precisely when the Premier League exploded worldwide, an entire generation of global fans grew up supporting the actual elite, leaving your self-generated revenue and sponsorships miles behind the clubs you want to be compared to."

**Label:** analysis

> "I just want to say, if Kosovo qualify today it would be an amazing achievement, and one that was very hard earned.
>
> In a group of Switzerland, Sweden, and Slovenia, they managed to finish 2nd place to make the playoffs. And while that group may not have included a traditional European powerhouse, there isn't a single easy game there.
>
> Kosovo came in as the 4th seed in that group, and while Switzerland were the 2nd-to-last pot 1 team, Sweden and Slovenia were both the 2nd highest seeded teams of pot 2 and 3.
>
> When the group started, Kosovo had Switzerland away and lost 4-0 their first match. But they didn't care and won home and away to Sweden and beat Slovenia away to get 2nd, and even drew 1-1 to a qualified Switzerland in their last match to finish strong.
>
> Then in the qualifiers they beat Slovakia in a thrilling 3-4 match where they were down 2-1 at halftime, but dominated the 2nd half to score 3 goals in a row to win it.
>
> For those wondering, of the 8 games played in the playoff matches, the home side won 5 of them, with the 3 away winners being Sweden, who played Ukraine in a neutral ground, so not even away, and Bosnia, who beat Wales on pens away. So that just shows the challenge Kosovo had to overcome to win vs Slovakia (A Slovakia that also beat Germany 2-0 at home in their qualifier group).
>
> And now all they need to do is beat Türkiye to qualify for the WC to make a group with USA, Paraguay, and Australia (which would lowkey be the weakest World Cup group of all time but the fans of those countries will probably be happy).
>
> Either way, this is a country that declared independence in 2008, one that when Spain play, they don't even capitalize the letters KOS because they dispute their independence, and they might somehow qualify for a World Cup as a top 16 European team, when they haven't even played a Euros! Not only that, they only became a FIFA member in 2016, and this is only their 5th time in a qualifiers for a tournament.
>
> Either way this has been a crazy campaign, it'll be crazy to see what happens vs Türkiye!"

**Label:** analysis

---

### 2. hot_take

**Definition:** A bold, confident opinion stated without supporting evidence. The claim might be true, but the post asserts rather than argues.

**Examples:**

> "Ronaldo is a terrible captain. How hard is it to make a statement to stop harassment of fellow teammates? He clearly supports this toxic behavior and even uses his sisters as mouthpieces.
>
> I don't even care if my country gets worse at football but the day we go back to only 10M 'supporters' when Ronaldo retires is the best day ever."

**Label:** hot_take

> "This Czech team is my least favourite team in the whole World Cup. They should be a solid European team with players like Sulc, Schick and Soucek, but they play the same football as clubs in the Iraqi League. Just a bunch of corner and throw in merchants that feel allergic to victory"

**Label:** hot_take

---

### 3. reaction

**Definition:** An immediate emotional response to a specific event. Little to no argument — the post is expressing a feeling in the moment.

**Examples:**

> "Australia played really well last night. That US Australia game will be a cracker, im really interested to see how Poch sets up the attack and how the Aussie defense will contain it"

**Label:** reaction

> "Goretzka is so useless man, was on the pitch for 10 minutes and even in that time you could see how out of his depth the guy was"

**Label:** reaction

## Data Collection Plan

I will collect examples from r/soccer. Within r/soccer there is a tag for discussion posts. Every day there is daily discussion post where people discuss the current happenings in soccer. I've found this to be a good place to get people's takes. I'm going to keep collecting posts until I reach 200 posts with balanced classes. So that will mean about 66 posts per label. I don't suspect I'll have much trouble getting an even class balance because there is so many posts I could go through to find the posts that I think fit the labels correctly.

## Labelling Process

The labeling for the posts was done manually by me. I'm a big soccer fan so it was easy to label the posts quite quickly. I did have to try my best to make sure I wasn't being biased and was labelling things fairly. Of course, because the labels were done by a person there is some subjectivity in the labels. However this is hard to completely avoid while still maintaining accuracy because takes are inherently subjective.

## Label Distribution

I tried my best to avoid any class imbalance issues. I believe that in the final dataset the classes are completely balanced. It wasn't too difficult to find posts which fit each label because I use r/soccer in my personal life so I had a good idea of where to look if I wanted for example analysis posts/comments versus more hot takes.

## Difficult Labeling Examples

**#1**

> "Silve has to be one of the least injury prone player ever.
>
> Bernardo Silva has 45+ appearances every single season for Manchester City, for 9 years in a row."

**Label:** analysis

**Explanation:** This post might be a hot take depending on whether or not you feel like the argument is well supported. I don't think the claim is very bold and I thought that the statistic about appearances was enough for me to label this as analysis rather than a hot_take.

---

**#2**

> "That Strand-Larsen fee is downright hilarious. Gives me hope maybe our new chairman will be better at negotiating outgoings because what the fuck are Palace doing."

**Label:** reaction

**Explanation:** I labelled this post as a reaction but I think that a model without much soccer context and inference capabilities might label this as a hot_take. The reason that this is a reaction is because it is in reaction to a fee a club paid to sign Strand-Larsen, and this can be indirectly inferred from the text. If the model is not able to make this inference than it might just label the post as a hot_take.

---

**#3**

> "Alvaro Arbeloa is misusing Bellingham. Jude is obviously an inverted false 6 with a metaphysical attacking mindset, operating in interdimensional half-spaces. He's basically a rotational inverse 8.5 who breaks lines through resonant vibrations whenever he's aligned with Jupiter."

**Label:** hot_take

**Explanation:** I think that this post clearly makes a bold claim. However it could be argued that this should be analysis because the argument is well supported with tactical reasoning. I decided to label this as a hot_take because I don't think the evidence was enough to support this bold claim.

## Baseline Description

The baseline model I used was Groq. The training platform I will be using is Colab. I split my dataset into training, testing, and validation sets. Then I ran Groq on 30 examples from the testing set with the following system prompt:

```
You are classifying reddit posts from r/soccer.
This is a community that is focused around the discussion of the sport soccer.
Assign each post to exactly one of the following categories.

analysis: the post makes a structured argument backed by statistics, historical comparison, or tactical observation. Evidence is specific and verifiable.
Example: "I just want to say, if Kosovo qualify today it would be an amazing achievement, and one that was very hard earned.

In a group of Switzerland, Sweden, and Slovenia, they managed to finish 2nd place to make the playoffs. And while that group may not have included a traditional European powerhouse, there isn't a single easy game there.

Kosovo came in as the 4th seed in that group, and while Switzerland were the 2nd-to-last pot 1 team, Sweden and Slovenia were both the 2nd highest seeded teams of pot 2 and 3.

When the group started, Kosovo had Switzerland away and lost 4-0 their first match. But they didn't care and won home and away to Sweden and beat Slovenia away to get 2nd, and even drew 1-1 to a qualified Switzerland in their last match to finish strong.

Then in the qualifiers they beat Slovakia in a thrilling 3-4 match where they were down 2-1 at halftime, but dominated the 2nd half to score 3 goals in a row to win it.

For those wondering, of the 8 games played in the playoff matches, the home side won 5 of them, with the 3 away winners being Sweden, who played Ukraine in a neutral ground, so not even away, and Bosnia, who beat Wales on pens away. So that just shows the challenge Kosovo had to overcome to win vs Slovakia (A Slovakia that also beat Germany 2-0 at home in their qualifier group).

And now all they need to do is beat Türkiye to qualify for the WC to make a group with USA, Paraguay, and Australia (which would lowkey be the weakest World Cup group of all time but the fans of those countries will probably be happy).

Either way, this is a country that declared independence in 2008, one that when Spain play, they don't even capitalize the letters KOS because they dispute their independence, and they might somehow qualify for a World Cup as a top 16 European team, when they haven't even played a Euros! Not only that, they only became a FIFA member in 2016, and this is only their 5th time in a qualifiers for a tournament.

Either way this has been a crazy campaign, it'll be crazy to see what happens vs Türkiye!"

hot_take: a bold, confident opinion stated without supporting evidence. The claim might be true, but the post asserts rather than argues.
Example: "Ronaldo is a terrible captain. How hard is it to make a statement to stop harassment of fellow teammates? He clearly supports this toxic behavior and even uses his sisters as mouthpieces.

I don't even care if my country gets worse at football but the day we go back to only 10M 'supporters' when Ronaldo retires is the best day ever."

reaction: an immediate emotional response to a specific event. Little to no argument — the post is expressing a feeling in the moment.
Example: "Australia played really well last night. That US Australia game will be a cracker, im really interested to see how Poch sets up the attack and how the Aussie defense will contain it"

Respond with ONLY the label name.
Do not explain your reasoning.

Valid labels:
analysis
hot_take
reaction
```

## Fine-tuning Approach

The model I used was dilbert-base-uncased. The training platform I used is Colab. One hyperparameter decision I decided to change was the learning rate. I made the decision to reduce it in order to improve performance.

## Evaluation Report

### Base Model Performance

Evaluated on 30 posts  
**Baseline Accuracy:** 0.933

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| analysis | 0.92 | 1.00 | 0.96 | 11 |
| hot_take | 1.00 | 0.90 | 0.95 | 10 |
| reaction | 0.89 | 0.89 | 0.89 | 9 |
| **accuracy** | | | **0.93** | **30** |
| macro avg | 0.94 | 0.93 | 0.93 | 30 |
| weighted avg | 0.94 | 0.93 | 0.93 | 30 |

### Fine-tuned Model Performance

**Model Accuracy:** 0.833

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| analysis | 1.00 | 0.91 | 0.95 | 11 |
| hot_take | 0.78 | 0.70 | 0.74 | 10 |
| reaction | 0.73 | 0.89 | 0.80 | 9 |
| **accuracy** | | | **0.83** | **30** |
| macro avg | 0.84 | 0.83 | 0.83 | 30 |
| weighted avg | 0.84 | 0.83 | 0.83 | 30 |

### Confusion Matrix

| True \ Predicted | analysis | hot_take | reaction |
|------------------|----------|----------|----------|
| **analysis** | 9 | 1 | 0 |
| **hot_take** | 4 | 4 | 2 |
| **reaction** | 2 | 1 | 7 |

### Wrong Predictions

| # | Text | True Label | Predicted | Confidence | Analysis |
|---|------|------------|-----------|------------|----------|
| 1 | "England have the best squad on paper at this World Cup and they'll still bottle it because they always do. I'd put my house on a quarter-final exit. Some things never change." | hot_take | reaction | 0.77 | The post makes a bold claim based on no evidence. It can't be a reaction because it's not reacting to any specific event that occurred. The model may have interpreted this as a reaction to an England game. |
| 2 | "Since Saka came back from injury he has 2 goals and 3 assists in 6 games despite the fact he's very obviously still hampered by injuries. Also has 3 goals and 1 assist in 5 World Cup games, for comparison Foden has 4 England goals in 49 games, Bowen has 1 goal in 22 games. I sadly think he's not gonna get back to the level he could have reached/did reach last season pre injuries but he's still a very good player and there's not many wingers better than him." | analysis | hot_take | 0.84 | The post makes a structured argument based on statistics. The model may have read the last sentence and labeled it a hot_take because it thought the claim that Saka will not reach the level of last season wasn't sufficiently supported by the evidence. |
| 3 | "Van de Ven's head was like a magnet for the ball. Tottenham defended excellently, they were so well drilled and every player put in a shift and happily took on defensive duties. Really impressive when you consider the main complaint with Ange is his team's lack of defensive structure and coaching." | reaction | hot_take | 0.94 | The post is in reaction to a specific game, which is clear in the words "Tottenham defended excellently." The model may have missed that detail and labeled it hot_take. That level of inference might not be there for this model quite yet. |

### Label Confusion Analysis

Format: [True Label → Predicted Label]

The only pairs with 0 or 1 errors were [analysis → reaction] and [reaction → hot_take]. The most common mistake was [hot_take → analysis].

| Label Boundary | Why It's Hard | Potential Fix |
|----------------|---------------|---------------|
| hot_take → analysis | There's no clear line between what is enough/sufficient evidence for an argument to be well supported (analysis) or cherry picked (hot_take) | More training data to better learn the evidence threshold; the model may improve with a larger dataset |
| reaction → hot_take | A reaction has to be in reference to a specific event, but people often react without directly stating the event — many reaction posts only indirectly reference a specific event | More training data and improved contextual inference so the model can detect indirect event references |

## Sample Classifications

**Text:** "Benzema isn't legend of French National Team. He never won anything significant with them (World Cup or EURO), he performed worse than Griezmann, Mbappe and even Giroud was more useful. He also blackmailed his fellow international player Valbuena. I am not sure if I should add Ribery here as well."  
**Predicted Label:** hot_take  
**Confidence Score:** 0.86  
**Explanation:** This is a hot_take because it makes a bold claim ("Benzema isn't a legend of the French National Team") and it provides very little statistical or historical evidence to support that claim.

---

**Text:** "Losing the final on penalties shouldn't erase what was a strong Arsenal campaign. They conceded the fewest goals of any side in the knockout phase, took the eventual winners to a shootout, and were the better team for long stretches of extra time before Eze and Gabriel missed. Shootouts are close to a coin flip once you reach them and the conversion data under fatigue bears that out. Judging a whole season on five spot kicks is exactly the recency bias that gets managers sacked unfairly."  
**Predicted Label:** analysis  
**Confidence Score:** 0.93

---

**Text:** "Watching us go out on penalties again has broken something in me. Twelve years following this team and it's always the exact same gut punch. I don't even have words tonight."  
**Predicted Label:** reaction  
**Confidence Score:** 0.86

## Reflection

I intended for the model to be able to capture the nuances of people's soccer takes and accurately label them. I think that the model ended up capturing the labels very well in more clear cut cases. It seems like those borderline decisions where the model would need to infer a bit and do some deeper reasoning to come to the correct label gave the model trouble. There are also some cases where a take can be both reactionary and a hot_take and depending on the definition of the labels and the interpretation of the model it can go either way. Some of the nuances which can help distinguish between hot_take and reaction were missed by the model in some cases. I also think that there are cases that domain knowledge in soccer itself is necessary to distinguish whether an argument is well supported or cherry picking facts out of context. That is the difference between analysis and hot_take.

## AI Usage

### AI Tool Plan

| Task | Tool | Input | Expected Output | Verification Method |
|------|------|-------|-----------------|---------------------|
| Label stress-testing | Claude | Label definitions and edge case descriptions | 10 posts at the boundary between two labels | Classify the posts and adjust label definitions if needed |
| Annotation Assistance | N/A | — | — | — |
| Failure analysis | Claude | Examples of posts the trained model got wrong | Patterns and reasons for incorrect labels | Run the model multiple times in different sessions to see if the patterns persist |

### Instances Where I Used AI

I used Claude to help determine what my labels were. I also used Claude to improve my label definitions. I asked Claude to provide me some examples of posts that might be borderline and labelled incorrectly because of a flaw in my current label definitions. This helped me change my definitions and the examples I provided to be more specific.

I used Claude to help adjust the hyperparameters for the fine tuning. Claude recommended changes to the numbers of epochs, the learning rate, and the warmup. I actually overrode Claude's suggestion to have 15 epochs because I thought that might cause too much overfitting. I did implement Claude's recommendations to reduce the learning rate a bit and change the warmup_ratio.

## Spec Reflection

I think the spec was very helpful this project in helping me stay organized. This was useful because I completed this project over multiple days so it was nice to have something to look back at and remember what still needs to be done. I do think that the spec was less helpful for this project compared to the previous two because there was no coding, so the spec wasn't needed in order to give context to Claude Code. I generally kept in line with my spec and didn't diverge from it.
