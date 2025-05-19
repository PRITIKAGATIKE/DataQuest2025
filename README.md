# DataQuest2025
##Overview:
The corporation has spent numerous resources and has wasted large amounts of money on meeting overviews written by trained professionals who could better use their time on more complex tasks. Not to mention, the need for follow-up emails, chats, and note-taking has wasted valuable company time. And hence, we introduce our model- StreamLine, ideated to streamline the redundant tasks that could be automated to make the employee’s life easier, and more importantly-accurate. Reducing the scope for human error in follow-up emails after meetings: by presenting accurate transcription summaries, active AI-powered solutions, and giving a personalised efficiency index, StreamLine is here to remove the mundane tasks that no employee wants to do. 

StreamLine is being built on VS Code using Langchain, Poetry, and Python technologies. We have incorporated Agentic AI-powered features that have been explained in detail below. Using the Parallel chain, branch chain, and RAG, we have been able to see a systematic breakdown of complex hour-long meetings, emails, calendar updates, and even chat logs.
 
![image](https://github.com/user-attachments/assets/63645c65-91b3-418c-aee5-52a0cc355134)



##Features of Summary:

### Default Summary of Google, Zoom, or Professional call transcripts 
The model will generate a default summary of the meeting (and email chains), which will be beneficial not only to the members of the team who may have missed the meeting but also to the attendees. It has been programmed to send an email to every team member, consisting of a concise summary of the meeting, which will help record the new ideas and projects that may have spontaneously been brainstormed. The summary includes the following features :
Main Conclusions
Pros and Cons
Meeting Efficiency
Assigning Tasks

### Main Conclusions 
The most productive meetings are those with spontaneous ideas, giving space for creativity and innovation. However, the challenges that most corporate meetings encounter are strict adherence to the agenda, ensuring easy note-taking. However, if our model can handle note-taking, the attendees will have more time to freely think and nurture their minds.
During creative sessions, ideas are swapped, and it's often confusing to many employees what the final decision is and what tasks are to be done. So our model will give all the main conclusions of the meeting.  It also includes the new agendas to be met in future meetings as discussed in the transcription.



### Pros and Cons: 
Our model analyses the transcripts and gives the pros and cons of the ideas discussed in the meeting. The pros and cons discussed in the meeting are taken down, and further points are generated using AI reasoning to give the team a broader understanding. With the implementation of our parallel chain using Langchain libraries, our model will be able to return the results that we desire. Furthermore, our agent will have tools such as internet searching and query database to look at previous ideas from other meetings that could potentially overlap.
![image](https://github.com/user-attachments/assets/205d3ffb-98a9-48c5-a4c2-f0320f05617a)


### Efficiency Index
A large company’s primary goal is to provide its service or product with the highest quality and lowest cost of production, and the efficiency of its employees plays a vital role in the achievement of this goal. Our model has been designed to calculate whether this meeting has met the agendas and managed the corporate flow of the meeting. Hence, a report will be generated for a corporation, which includes how much time has been wasted during the meeting and how much time is taken for each agenda, and whether all agendas have been met, ensuring that the employees stay on track during this long meeting.

This will be done through a branch chaining, similar to this:
![image](https://github.com/user-attachments/assets/ab0fe9b1-de54-442c-98e9-8466afe23a07)



### Assigning Task:
Our model aims to help managers and team leads have a more streamlined and efficient workspace by analysing the meeting transcripts and noting down any work that has been assigned verbally during the meeting. This will help team members remember their tasks and avoid the requirement to send out official emails and further chats in order to ensure that the work assignment has been conveyed. 
We will be using a Retrieval Augmented Generation, with “similarity” retrieval.

The user query/prompt:
“Display {assigned tasks} that have been given to {Team member name}, this includes {addition details about task}”


## Additional Features
## Additional Questions:
We plan to incorporate a small chatbot at the end of the meeting to facilitate additional questions. If any team member has logged off for a specific amount of time or missed parts of the meeting due to connectivity issues, they can question the bot and get additional personalised information without having to read the entire transcript.
This method will also contain RAG and character splitting, however, it will not be in a parallel chain with the rest of the tools under summary.
Ex:
System: Interaction with members of the team involved in the meeting is conducted
Human:{Query}
*User query sent to AI agent executor*

### Skill matching:
If the meeting agendas require the need for extra personnel to be involved in any upcoming project or tasks, we hope to have our agent connected to a tool that is directly synced with the company database( listing personnel availability and skills) inorder to seamlessly find the required members without manual searching and excessive and unnecessary emails to wrong members, streamlining and increasing efficiency by pushing projects forward.

Our flow will look very similar to this:
![image](https://github.com/user-attachments/assets/cf76bb12-961f-46b5-821d-f7fb709491eb)



##Open Ended Questions:
In many meetings/email chains/chat logs, there may be important questions that have been discussed but ultimately left unanswered, and these questions will all be documented under a separate section. Some of these questions will have potential answers discussed in the meeting, and some will have AI-powered solutions related to previous such queries and the progression of the meeting.

A few questions could be:
-When should we have our next meeting?
Our Agent will have tools that will have access to the employee's calendar, reducing the burden of discussing the actual date of the meeting, as AI will find the optimal solution. Especially in scenarios where there are more than 5 members.
-What is the next plan of action?
The system may respond like this:
Team member 1 has suggested Plan A, with 23 people’s agreement.
Team member 2 suggested Plan B, with 22 people’s agreement.
Our AI tool has seen an issue similar to this in the previous meeting and will suggest Plan C, and believes that Plan B has more pros than cons compared to Plan B as discussed in the auto-generated summary.


##Chat Logs:

Unlike meetings and emails, chat logs do not have the same organic flow, which is why for chat logs we will not be using character spitting and will opt for recursion splitting according to the discussed topic. For the summary of chats, the user will have to enter a query; we have not opted for auto-generation, as numerous different topics (unrelated to work yet extensively discussed) also might be discussed, and hence the user will have to request the summary of the specific topic.

We believe that this feature can be further integrated with WhatsApp chats and numerous other applications according to user requirements.

##System Architecture:


![LL](https://github.com/user-attachments/assets/6e6a5f6b-4cc9-484d-b858-92c926c8d339)





