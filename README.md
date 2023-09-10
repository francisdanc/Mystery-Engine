# Mystery-Engine
[Introduction](#introduction)

[Original Idea](#original-idea)

[Approach](#figuring-out-an-approach)
# Introduction 
I've always enjoyed the mystery genre, theres something about solving a mystery that is really satisfying to me. I remember as a kid playing the Professor Layton series by nintendo and enjoying racking my brain trying to solve puzzles all the while trying to figure out the mystery that drove the story or reading every book in Anthony Horrowitz, Diamond Brothers Detective Agency book series. I thought to myself recently that i'd enjoy a mystery game in which I could really feel like a detective, in which i question suspects, try and figure out motives and piece together a story of what happened. I've come to find that no such game exists, there are some that come close but they ultimately fall short and become repetetive or dont require any real aspects of what appeals to me about the detective genre such as motive and character. 

# Original Idea
This need for a detective experience led to the idea of the Mystery Engine! The Mystery Engine will take a set of inputs and given these inputs the Mystery Engine (I will go into depth about proposed methodology later) will generate a mystery story in which there is a victim, a culprit, a method of murder and a motive all within a set location. The user will then be able to question characters about the event that took place and inspect the crime scene in order to piece together a story and hopefully arrest the correct suspect.

# Figuring out an appraoch
The first step to creating TME (The mystery engine, i will refer to it as TME from here on out) is to figure out the user experience. Currently i'm imagining a text based adventure, giving a sort of dungeons and dragons-esque experience in which there is complete freedom for the user to explore the mystery that has been created around them. Though there should be some restrictions, for example the user should be constricted in a set area in which the crime took place (however in the future it may be fun to think about a larger scope). So the input to the network then would be a string of text from the user, describing what they would like to do, in response the system should describe what has happened because of the users action. What information then should the system hold in order to create a cohesive story for the user to follow? 

1) The system should hold a complete description of the crime that took place and how it happened
2) The system should hold a map of the location in which the story is taking place
3) The system should have a timeline of events for each character within the story, along with a daily routine
4) The system should also hold character details, such as personality, relationships to other characters, occupations and potentially visual descriptions
5) The system also needs a way in order to remember the actions a user has taken, perhaps not every action, but anything that effects the other elements, such as interactions with characters or the environment

So how much is pre-defined and how much is generated by the system? I suppose this depends upon the data that I can gather. Originally I thought about taking mystery books such as Sherlock Holmes or Agatha Christy novels and using those to generate a mystery, however while reading it came to my attention that these stories are saturated with a lot of unnecessary data. which begs the question which parts of these stories are important in order to create a satisfying mystery? Or in other words how much can be taken away and still create a meaningful story? Thinking in terms of a detective, the only things that are important in regards to a mystery are **_how it happened, who it happened to, why it happened and who did it_**. Okay so then all I need to do is look at famous mysteries, and answer all of these questions, some other things that i need additionally for my system are location and suspects. The other things i mentioned such as personality and occupation I can just get from other sources. So now I have list of things i need to collect.
1) How was the crime commited
2) Who was the victim
3) What was the motive
4) Who was the culprit (Not only who they were in terms of name, but moreover who were they in relation to the victim and the story)

### Data Structures
So now all of that is figured out I need to decide how i'm going to store the data
