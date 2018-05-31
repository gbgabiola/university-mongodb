# Lab 1.1: Install Compass and Connect

## Problem:
If you have not yet downloaded Compass, please follow these instructions. Then answer the question below.

1. Please download Compass from the [MongoDB Download Center](https://www.mongodb.com/download-center#compass).
2. Install Compass on your computer from the download.
3. Launch Compass.

When Compass opens you will see a page titled "Connect to Host".

![Compass Connect Screen](https://s3.amazonaws.com/edu-static.mongodb.com/lessons/M001/compass_connect_screen.png)

4. Use the following information to complete this form, but do not click "Connect" yet. Hostname is **cluster0-shard-00-00-jxeqq.mongodb.net**. Username is **m001-student**. Password is **m001-mongodb-basics**.
5. Click "Add to Favorites" so that you can easily connect to our class MongoDB deployment after closing and restarting Compass at some point in the future.
6. Now, click "Connect" and load the databases in the M001 class MongoDB deployment.

## Question:
Which of the following field names appear in documents in the movies collection of the video database. Check all that apply.

## Check all answers that apply:
1. _id
2. cast
3. comments
4. director
5. genre
6. length
7. plot
8. stars

## Answer:
1. _id
2. cast
4. director
5. genre
7. plot

## Detailed Answer:
In Compass, navigate to the schema view for the **movies** collection of the **video** database. Fields are listed in alphabetical order in the schema view and all fields found in the collection are listed in this view. Scroll through the schema view to check each choice to see whether it is present in documents in this collection.