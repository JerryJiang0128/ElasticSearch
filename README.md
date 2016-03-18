# ElasticSearch

A serach process in Kawo App has functionality which can relate the following inputs and outputs:
Input: a user click on a brand and type a text
Output: our app will return posts which can best match user's request

We need to design some algorithm to realize the above function. Generally, the alogrithm has two steps:
1. filtering data on elasticsearch server based on user's input
2. sort search results by order

Issues we need to solve:
1. Each brand may have up to hundreds of posts every day, it is not resonable to return all posts. We need to create some creteria to filter the posts
2. set up some rules to order the results
3. Posts in Kawo has three status: new, scheduled and publised. Which kind of status shall we choice right now? (this issue is optional right now)

Initial Solutions
We can write a query with following format:
{"query":
  {"match":{"brandId":"string"} and {"text": "some content") ordered by {"time":"date"}
}




  
