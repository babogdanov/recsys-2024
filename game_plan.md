0. Test random submissions as a sanity check
1. Simplify to multiple classification - given k possible articles inview, pick the one to put first
2. Content-based possibilities
 - build user profile from age, gender, etc...
 - measure similarity between articles that the user has interacted with and the ones inview for his interactions
3. Collaborative filtering
 - find "close" users, e.g. X has clicked on 10 articles and Y has clicked on 8 out of those 10, so we can recommend the remaining 2 to Y if they are inview
 - generate user:article table for each user and article; measure how much a person liked an article on fields like how much he scrolled in it, how much time did he read (history fields)

Naive content-based user profiles pseudocode:

for each article:
   put in object that supports comparing similarity with another article (tfidf or more complex)

for each article each user has interacted with:
   create user profile containing the vectorized articles (for example history df)
   
 for each user interaction:
    compare inview articles to articles he's already interacted with
   


   