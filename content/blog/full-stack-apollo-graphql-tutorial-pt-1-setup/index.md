---
title: 'Full Stack Apollo GraphQL Tutorial: Part 1 - The Setup'
tags: ["react", "nodejs", "graphql" ]
published: true
date: '2019-07-17'
---

Full Project Prerequisites: Ability to build a full-stack web app using Node and React, and a basic understanding of what GraphQL is. For further info, follow this link: [What is GraphQL](https://graphql.org/)<br>
Part 1 Prerequisites: Ability to set up a Node.js server with a framework such as Express.

Apollo GraphQL is an excellent platform for building full-stack GraphQL web applications. [Apollo Docs](https://www.apollographql.com/docs/) has a full-stack tutorial, but after completing it, I felt like there were too many gaps in my understanding of what I had picked up along the way. It spoon-feeds you so much at times, and gives you very little at others. That's why I'm doing this tutorial with the hope that it will makes things clearer the first time around for anyone who stumbles across this exercise and decides to come along for the ride. Rather than recreating that tutorial at Apollo Docs, I've constructed a simpler one that parallels theirs.

We'll use two data sources for our project, one an external API and the other an internal API. The external API comes from the US Geological Survey (USGS) and returns earthquake data. The internal one we'll make, and it'll be an API that returns information about registered users of the app, such as a user name, an email address, a user id, and a list of saved events (earthquakes). Since GraphQL is database-agnostic, we'll write a simple mock database along with data retrieval functions. We won't be using a state container like Redux for our project; we'll take advantage of the way that Apollo Client allows us to manage local state in the Apollo cache and query it in parallel with remote data using GraphQL. 

