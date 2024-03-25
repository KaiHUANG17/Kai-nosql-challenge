# Kai-nosql-challenge
## Instructions
- The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Part 1: Database and Jupyter Notebook Set Up
- Use NoSQL_setup_starter.ipynb for this section of the challenge.
Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.
Within your notebook, import the libraries you need: PyMongo and Pretty Print (pprint).
Create an instance of the Mongo Client.
Confirm that you created the database and loaded the data properly:
List the databases you have in MongoDB. Confirm that uk_food is listed.
List the collection(s) in the database to ensure that establishments is there.
Find and display one document in the establishments collection using find_one and display with pprint.
Assign the establishments collection to a variable to prepare the collection for use.

## Part 2: Update the Database
- Use NoSQL_setup_starter.ipynb for this section of the challenge.
The magazine editors have some requested modifications for the database before you can perform any queries or analysis for them. Make the following changes to the establishments collection:

## Part 3: Exploratory Analysis
- Eat Safe, Love has specific questions they want you to answer, which will help them find the locations they wish to visit and avoid.
Use NoSQL_analysis_starter.ipynb for this section of the challenge.
Some notes to be aware of while you are exploring the dataset:
RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.
Note: This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating. We will coerce non-numeric values to nulls during the database setup before converting ratings to integers.
The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.
Use the following questions to explore the database, and find the answers, so you can provide them to the magazine editors.

## References
- update_result = establishments.update_many(
    {},
    [
        {
            '$set':
            {
                'geocode.latitude': {'$toDouble': '$geocode.latitude'},
                'geocode.longitude': {'$toDouble': '$geocode.longitude'}
            }
        }
    ]
)
- chatgpt "https://chat.openai.com/c/a0969e89-6fd5-49b0-8636-44bbab2094ce"

