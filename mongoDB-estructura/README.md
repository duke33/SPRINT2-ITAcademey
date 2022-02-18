# We will model several entity-relationship diagrams.
# 2.3: MongoDB data structure

## Level 1
### - Exercise 1 - Optics
An optician called Cul d'Ampolla wants to computerize customer management and the sale of glasses:

First of all the optician wants to know which is the supplier of each of the glasses. Specifically, you want to know the name, address (street, number, floor, door, city, postal code and country) of each provider, telephone, fax, NIF.

The optical purchasing policy is based on the fact that glasses from one brand will be bought from a single supplier (so you can get better prices), but they can buy glasses from several brands from one supplier. From the glasses you want to know, the brand, the graduation of each of the glasses, the type of frame (floating, paste or metal), the color of the frame, the color of the glasses and the price.

Customers want to store their name, mailing address, phone number, email, and registration date. We are also asked, when a new customer arrives, to store the customer who has recommended the establishment (as long as someone has recommended it). Our system will need to indicate who and when the employee has sold each pair of glasses.

### - Exercises 2 - Pizzeria
A customer has hired you to design a website that allows you to place food orders online:

Please note the following instructions for modeling the project database: We store a unique identifier for each client, first name, last name, address, zip code, location, province, and phone number. Location and province data will be stored in separate tables. We know that a locality belongs to a single province, and that a province can have many localities. For each location we store a unique identifier and a name. We store a unique identifier and name for each province.

A customer can place many orders, but a single order can only be placed by a single customer. Each order stores a unique identifier, date and time, if the order is for home delivery or in-store collection, the number of products selected for each type and the total price. An order may consist of one or more products.

Products can be pizzas, burgers and drinks. Each product is stored: a unique identifier, name, description, image and price. In the case of pizzas, there are several categories that can change their name throughout the year. A pizza can only be in one category, but one category can have many pizzas.

A unique identifier and a name are stored for each category. An order is handled by a single store, and one store can handle many orders. Each store has a unique identifier, address, zip code, location, and province. Many employees can work in one store and one employee can only work in one store. Each employee is stored a unique identifier, name, surname, nif, telephone and whether he works as a cook or delivery man. For home delivery orders, it is important to save the delivery person who delivers the order and the date and time of delivery.

## Level 2
### - Exercise 1 - Youtube
We'll try to make a simple model of what the database would look like for a reduced version of YouTube:

We store a unique identifier for each user, email, password, username, date of birth, gender, country, zip code. A user posts videos. We store a unique identifier for each video, a title, a description, a size, the name of the video file, the length of the video, a thumbnail, the number of plays, the number of likes, the number of dislikes.

A video can have three different states: public, hidden, and private. A video can have many tags. A tag is identified by a unique identifier a tag name. It is important to save the user who posted the video and on what date / time. A user can create a channel. A channel has a unique identifier, name, description, and creation date. A user can subscribe to other users' channels. A user may like or dislike a video only once. It will be necessary to keep a record of the users who have liked and disliked a certain video and on what date / time they did it. A user can create playlists with the videos they like. Each playlist has a unique identifier, a name, a creation date, and a status that indicates that it can be public or private. A user can write comments on a particular video.

Each comment is identified by a unique identifier, the text of the comment, and the date / time it was posted. A user can mark a comment as they like or dislike. It will be necessary to keep a record of the users who have marked a comment as I like / dislike, and on what date / time they did so.

## Level 3
### - Exercise 1 - Spotify
We will try to make a simple model of what the necessary database for Spotify would look like:

There are two types of users: free user and premium user. We store a unique identifier for each user, email, password, username, date of birth, gender, country, zip code.

Premium users subscribe. The necessary data to be saved for each subscription are: subscription start date, service renewal date and a form of payment, which can be by credit card or PayPal.

From credit cards we keep the card number, month and year of expiration and the security code. For users who pay with PayPal, we keep the PayPal username. We are interested in keeping track of all payments that a premium user has been making during the period they are subscribed to. The date, an order number (which is unique) and a total are saved for each payment.

A user can create many playlists. From each playlist we keep a title, the number of songs it contains, a unique identifier and a creation date. When a user deletes a playlist, it is not deleted from the system, but is marked as deleted. This allows the user to retrieve their playlists if they have been deleted in error. It is necessary to store the date on which a playlist was marked as deleted.

We can say that there are two types of playlists: active and deleted. An active playlist can be shared with other users, which means that other users can add songs to it. In a shared list we want to know which user added each song and on what date. A song can only belong to a single album. An album can contain many songs. An album has been released by a single artist. An artist may have released many albums. Each song has a unique identifier, title, duration, and number of times it has been played by Spotify users.

For each album we keep a unique identifier, title, year of publication and an image with the cover. For each artist we keep a unique identifier, name and image of the artist. A user can follow many artists. An artist may be related to other artists who make similar music. So Spotify can show us a list of artists related to the artists we like. We're also interested in saving a user's favorite albums and songs. A user can select many albums and many songs as favorites.

To verify your design, populate the tables with test data to verify that the relationships are correct