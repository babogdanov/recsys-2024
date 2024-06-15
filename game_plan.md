-1. Test random submissions as a sanity check
1. Simplify to multiple classification - given k possible articles inview, pick the one to put first
2. Content-based possibilities
 - build user profile from age, gender, etc...
 - measure similarity between articles that the user has interacted with and the ones inview for his interactions
3. Collaborative filtering
 - find "close" users, e.g. X has clicked on 10 articles and Y has clicked on 8 out of those 10, so we can recommend the remaining 2 to Y if they are inview

for each article:
   put in object that supports comparing similarity with another article

for each article each user has interacted with:
   create user profile containing the vectorized articles 
   
 for each user interaction:
    compare inview articles to articles he's already interacted with
   
    