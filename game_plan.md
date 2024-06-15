0. Test random submissions as a sanity check
1. Simplify to multiple classification - given k possible articles inview, pick the one to put first
2. Content-based possibilities
 - build user profile from age, gender, etc...
 - measure similarity between articles that the user has interacted with and the ones inview for his interactions
3. Collaborative filtering
 - find "close" users, e.g. X has clicked on 10 articles and Y has clicked on 8 out of those 10, so we can recommend the remaining 2 to Y if they are inview
 - generate user:article table for each user and article; measure how much a person liked an article on fields like how much he scrolled in it, how much time did he read (history fields)

 User2Vec
- User embedding from their age, location, etc. Can be included in user profile concept for content-based
 Имаме user с inview от статии 1, 5, 10. Търсим всички user-и, които са имали същите статии в inview (или само някои от тях, ама е по-сложно). Мерим близост на векторите на user-ите и намираме най-близките до нашия user. Спрямо това топ 10 user-ите дали са отворили или неотворили, решаваме дали нашия човек ще отвори статиите.

Naive content-based user profiles pseudocode:

for each article:
   put in object that supports comparing similarity with another article (tfidf or more complex)

for each article each user has interacted with:
   create user profile containing the vectorized articles (for example history df)
   
 for each user interaction:
    compare inview articles to articles he's already interacted with
   


   