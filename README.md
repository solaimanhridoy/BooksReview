![](/home/lib10/Insync/hridoy341@gmail.com/Google Drive/Courses and Projects/My Projects/06. BooksReview/img/frontlook.png)

# Dot-Book

"*A web application to give reviews and ratings to books.*"

Step by step to run this flask web applications on linux machine:

1. Clone the repository to your local machine:

```
git clone https://github.com/solaimanhridoy/BooksReview.git 
```

2. Run terminal from the project repository and type:

```
export FLASK_APP=application.py
```

3. Then export environment variable to the database url, type:

```
export FLASK_ENV=DATABASE_URL
```

4. Set the database url:

```
export DATABASE_URL="postgres://aubfrchzhbbjxz:8d68924dca3426e924f83feeed9de6f6e766bc71accf8c068f6e12b3cb3c13fe@ec2-23-21-130-182.compute-1.amazonaws.com:5432/dau1vei0b9q2ng"
```

5. Finally run flask server:

   ```
   python3 -m flask run
   ```

   ### App Description 

- At the point when you start this application first time you will be diverted to the login page where you can join and sign in. 

- login.html record expands layout.html. There are two structures on the login page, one for enrolling a second for signing in.

- The JavaScript function checks if passwords coordinate during sign up. 

- After successfully sign up you can attempt sign in. Once you are signed in the username shows close to log out catch.

- Then you will be redirected to index.html after logged in. Now you will see simple quote and will be able to search books database. 

- If you search for the books the list of books will be shown. Clicking one of the positions takes you to the book page.

  *example:* Search a  book name "A Touch of Dead" or "The Mark of Athena"

  *NB:* You will find more books name from the `books.csv` file.

- The book.html file extends layout.html. On the book page the author, year and isbn will be loaded and rating count and reviews from goodread.com API  itself will be loaded. 

- Then all reviews received from users along with ratings will be loaded one after one. At the bottom of the other comments you can leave your review and rating. 

- You can click the API button to generate json files.

- If you Click Log out button the session will be cleared and the will be logged out.

- The application.py file is the main app file. It contains routing to all html files, queries to database and all other functions.

- The helpers.py file contains one function, that search if there is data in session. If there is no data found it will redirect to log in page. 

- There is three tables -users, reviews, and books are created in the import.py file. 

- When books table is created it read csv file and loaded all the books from the goodread API.  
