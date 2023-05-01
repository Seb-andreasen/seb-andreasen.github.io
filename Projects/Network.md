## Recommendation engine using graph theory

**Project description:** 
In this project I am building a recommendation engine using graph theory. The hypothesis is that it is possible to connect people who likes the same kind of jokes based on jokes they have previously liked. 

### 1. Data source

The data source stems from [UC Berkeley](https://eigentaste.berkeley.edu/dataset/) and consists of 25.000 people who have each ranked between 36 and 100 jokes on scale from -10 - 10. 

The idea is that two people who has rated the same joke with a 9 or higher should be connected. 

To prepare the data I removed people who were above the 99% quantile in terms of rating the most jokes with a 9 or higher. I.e. if a person had rated all 100 jokes with a 9 or higher I would remove them from the data.

I then found the 1000 people who had rated the most jokes below the 99% quantile and used them as my sample. 

 To find these links I created the similarity matrix between all pairs of people and found the correlation between them: 


<img src="/images/carr_mat.jpg?raw=true"/>

As the results here are not very clear I converted the similarity matrix to a graph for further analysis. 

### 2. The analysis

Each node in the network is a person who has rated one or more jokes with a 9. There is an edge between nodes if two people has rated the same joke with a 9 or higher. 

I used the louvain algortihm to detect communities within the network and in this case I found 9 communities.


<br><br>

<img src="/images/network.jpg?raw=true"/>

For each community I found their favorite jokes, i.e.:
 
C1: 
A guy goes into confession and says to the priest, "Father, I'm 80 years old, widower, with 11 grandchildren. Last night I met two beautiful flight attendants. They took me home and I made love to both of them. Twice."
The priest said: "Well, my son, when was the last time you were in confession?"

"Never Father, I'm Jewish."

"So then, why are you telling me?"

"I'm telling everybody."

C2: 
The graduate with a Science degree asks, "Why does it work?"

The graduate with an Engineering degree asks, "How does it work?"

The graduate with an Accounting degree Asks, "How much will it cost?"

The graduate with a Liberal Arts degree asks, "Do you want fries with that?"

C9:
A man piloting a hot air balloon discovers he has wandered off course and is hopelessly lost. He descends to a lower altitude and locates a man down on the ground. He lowers the balloon further and shouts "Excuse me, can you tell me where I am?"
The man below says: "Yes, you're in a hot air balloon, about 30 feet above this field."

"You must work in Information Technology," says the balloonist.

"Yes I do," replies the man. "And how did you know that?"

"Well," says the balloonist, "what you told me is technically correct, but of no use to anyone."

The man below says, "You must work in management."

"I do," replies the balloonist, "how did you know?"

"Well," says the man, "you don't know where you are, or where you're going, but you expect my immediate help. You're in the same position you were before we met, but now it's my fault!"

### 3. Future work

As we can see these jokes are all quite different and once a new person joins the network and starts rating jokes, we can assign this person to a community and start recommending more personalised jokes.

This is example is a toy example, but the logic and theory behind can be used for so much more such as recommendation engines for personalised content on websites, webshops, social media, etc. 

