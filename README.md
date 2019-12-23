
# The Nifty E-Commerce Store Final Project
_Special thanks to Tal Wolman for the original version of this project._

**Note: This is an adapted outline inspired by CSE 154 Summer Final Project. Edits made to it so the core parts of a full-stack project are here. You can see the original here**

## Overview
This Final Project will cumulate what you've been learning in the course with an opportunity to design, develop, and implement a full-stack website. You will be responsible for fully implementing both the front and back-end of an E-Commerce store of your choosing. Pick your theme, pick your features from the module component list, and have fun with it!

Please understand that this assignment is not a Creative Project. For full credit, this project must be clearly independent of your previous Creative Project (and HW) work. Ask the staff if you are unsure about similarity between previous assignments and your Final Project implementation.

Also, given the nature of this being a cumulative Final Project demonstrating the knowledge you have gained in this class, **you may not use online resources in this assignment**. This means, but is not limited to, using any online tutorials, code, videos or projects as a reference for yours. **Citing these resources does not make it acceptable to use them**. If you feel strongly that you would like to use a certain online resource you must get explicit permission from the instructor as well as explicitly cite the source. Similarly to CP code, any code based on or taken from an online resource will _not_ count towards the requirements for this assignment and may be subject to deductions without explicit permission.

Whatever you create for this project is yours to share as you choose meaning you can publish it and/or show it off to others. That being said, we strongly encourage you to have fun and go (reasonably) above and beyond with this assignment. It is your chance to not only show off the valuable skills you've learned, but also develop a strong portfolio piece. Happy coding!

## Starter Files and Deliverables

#### Proposal
Your proposal should include the items listed below:

  - Wireframe of UI (2 or more "views" sketched out or done with an online tool, no need to be an artist). The wireframe should be labeled with text to include what each piece of the view does, either to the side or below the wireframe diagram(s).
    - [Here](https://courses.cs.washington.edu/courses/cse154/19su/final-project/sample-wireframe.pdf) is an example of a wireframe for one "view" of a hypothetical e-commerce store. This should give you an idea of the level of detail we expect from you. These wireframes are meant to help your get an idea of what your project is and help you design both your front-end and the needs of your back-end, and are also valuable to include in any web development portfolio. We suggest that each view have a number indicator representing a piece of the view. Each piece can then have a description of what the said piece is and does.
  - You may find [Figma](https://www.figma.com/) and/or [draw.io](https://www.draw.io/) helpful for creating your wireframes.

  - Proposal Document which can he found [here](https://docs.google.com/document/d/1ZVwy88BuNltKpwfakHw_0J383j_TmQQVpH7eNt8qxGs/edit). You should make a copy of this document and answer the questions as prompted to in the document. The questions in  the document are meant to help you guide your thinking as you choose what type of e-commmerce store you are interested in implementing.

### Final Submission Requirements
Your Final Project repository contains no starter files outside of this `README.md` because you are choosing how to implement your nifty store. The repository for your final submission should be turned in with the files below:

| File | Repository file you will implement |
| --- | --- |
|`.html` | at least one `.html` file |
|`.css` | at least one `.css` file  |
|`.js` | At least one client-side `.js` file that will request the information from the server you've implemented and provide overall functionality to the page |
|`.js` | At least one `.js` file representing the Node.js/Express web service for your E-Commerce site  |
|`.sql`|  The `.sql` file that sets up the database/tables|
|`APIDOC.md`|The documentation file for your API|
|`CHOOSE.md`   |The documentation for the chosen features  |

**IMPORTANT NOTE:** All static "view" files (HTML/CSS/Client-side JS/any images) should be inside a "public" folder. All other files (e.g. your Node.js/Express web service) should be at the root, similar to the structure in HW4. You will almost definitely want to use images for your products - you can create your own, or find some online but you must cite where your images came from at the bottom of your HTML page. If you're not sure where to start, you can find some good "icon packs" on [flaticon.com](https://www.flaticon.com/) which has a [good overview](https://support.flaticon.com/hc/en-us/articles/207248209-How-I-must-insert-the-attribution-) of how to cite the icon sources for packs (you are free to use other images too).

Any files that were submitted for the milestone should be updated, if necessary, and pushed to your repository. Please do not include any files that are not relevant to your Final Project or include information in your `APIDOC.md` about an endpoint that is inaccurate and/or was not implemented.  

#### Front End  
- **Required Features**:
  - A way to see all of your service's products on a "main view" page
  - A way to see one product in a “single view” (at least 3 pieces of information such as the price/rating/name/colors/sizes it's available in etc.). You may choose to implement each "view" as a separate HTML page (e.g. index.html, contact.html, cart.html, etc.) or dynamically using JS/DOM manipulation.
    - The single view should be applicable and functioning for all products on your main view page.
  - A customer service view (e.g. contact page), which, at a minimum, must have a form for users to submit complaints/questions.
    - You must include some level of input validation (HTML5 or JS) to prevent invalid messages (such as empty messages) from being sent
      - This includes indications to the user (such as a message displayed on the screen) indicating that there is an issue with the form if all parts of the form are not filled out
      - You must also indicate to user that their message has been received
  - A way to filter through the products to only display ones with certain properties
    - This can either be accomplished with a search bar _or_ a dropdown/other UI elements that, once selected, only display products matching the chosen query
  - You must create a "cart" view which displays a list of items that the user is interested in
      - A user should be able to add/remove items from the cart
  - You must have at least 10 CSS rule sets in your `.css` file and 10 unique rules **at minimum**
    - Must change at least 2 box model properties (border, padding, margin, height, width)
    - Must import and use at least one font from [Google Fonts](https://fonts.google.com/)
    - Must use at least 2 flex properties (this excludes setting `display: flex`)
  - Must use `fetch` to communicate with the back-end (your web service)
    - Errors should be gracefully handled and displayed to the user (you may not use `alert`, `console.log` or `console.error`)

#### Back End
- **Required Features**:
  - Must have at least one JSON response (including a plain text response is optional)
  - Must have a `GET` endpoint to request and return all of your service's products
  - Must have a `GET` endpoint to request and return information about a single item
    - This endpoint should be functional for each item in your e-commerce store
  - Must have a `GET` endpoint to request and returns some of your service's products based on a filter (price, category, type etc.)
  - Must format the data from each request appropriately to send to the front-end (You should be able to explain why the way you designed your outputs are effective)
  - Must have a `POST` endpoint to accept and store all feedback received via customer service form (see front-end requirements)
  - Must have at least 2 tables in your SQL database - your database and table creation code should be defined in your `.sql` file.
  - Each table must contain at least 4 columns that are used in queries to store or retrieve useful data (id can count as one of these columns)
  - There should be at least 15 items in your E-commerce store (although we encourage you to add more to create a more interesting storefront).
    - These items should be inserted into the table in your `.sql` file using `INSERT` statements

#### Chosen Features
**OPTION 1**: An additional view indicating when/what promotions are available at your e-commerce store. There should be at least 5 promotions/sales available. All the information for the sales/promotions should be retrievable from a `GET` endpoint.

**OPTION 2**: A way for a user to buy a product/item from your e-commerce store. You should update the page indicating to the user the item has been sold and/or the order is on it's way. The updates to the stock of the item should be supported with a `POST` endpoint. Each time an item is bought the overall stock should be decremented.

**OPTION 3**: A way for a user to leave a review on an item. This review should be displayed on the page for other users to see and should be persistent across page reloads (using the appropriate storage technology). This feature should be supported with a `POST` endpoint so that each review left will be added to your database.

**OPTION 4**: An additional view in your e-commerce store so that users have a way of becoming "loyal customers." This should be achieved with a form and should  require at least three pieces of information from the customer (name, email, address, phone number etc.). Once a user joins successfully there should be a message displayed on the page indicating this. This should be supported with a `POST` endpoint so that all information on "loyal users" is added to your database.

**OPTION 5**: A way for a user to customize a product. The user should be able to customize at least two features such as color of the product, material of the product etc. These changes should be supported by a `POST` endpoint which updates the item description with the new customizations.

**OPTION 6**: An additional view for a FAQ page. This should have at least 5 frequently asked questions and the answers displayed on the page for customers to read. This should be supported by  a `GET` endpoint from which all the frequently asked questions and answers can be retrieved.

**OPTION 7**: An additional admin view allowing an administrator to add and/or remove items from the store as well as update current inventory. This should be supported with a `POST` endpoint which appropriately updates the database with the correct information based on whether the admin has added/removed an item from the store.

**OPTION 8**: An additional admin view for managing the accounts that the e-commerce store users have created. An admin should be able to edit a user account and modify information. This should be supported with a `POST` endpoint which will appropriately update the user information based on the administrator's actions.

### Internal Requirements
You are expected to follow the same Internal Requirements as the previous homework assignments you have completed. These include but are not limited to the following:  

- **HTML/CSS**
  - appropriate use of semantic tags
  - consistent and readable spacing/indentation/etc.
  - using classes/ids appropriately
  - not having duplicate rules in your css
  - using group selectors to group together shared styles
  - appropriate file documentation
- **Client-side JS**
  - Must aim to minimize the use of module global variables unless strictly necessary. Prefer minimizing and localizing the scope.
    - Ex: DOM elements should never be stored as module globals as you _always_ have access to them. Variables only used in one function should not be stored as module globals as it is completely unnecessary
  - Must use functions to minimize redundancy in your code
  - Must not have "do all" functions - instead break down into several functions such that each has a specific purpose
  - You should not make any unnecessary fetch requests
    - should not make a request before the information is required
    - should not make a request if the given information is already available
  - You must have appropriate documentation for all functions and for files.
- **Server-side JS**
  - should use async/await appropriately
  - choose correctly between the type of request (`GET` vs `POST`)
  - should not override content headers
  - should set error types appropriately
- **SQL**
  - Must define appropriate data types for each column in each table
  - Must have appropriate documentation
    - When documenting your SQL file, a brief header comment is sufficient with your student information and what the database/table(s) represent.

### Reflection Requirements
The reflection for this Final Project will be due on August 24th, 2019.  This document should be at least 1 page (double spaced, 12pt font, Times New Roman) and should be a reflection of your experience with the implementation process. Questions you could address are:
- What were the hardest features to implement? How did you approach these problems?
- What resources were most helpful to you (either provided by the course or found online)?
- Were there features you tried to implement and were unsuccessful? What were they and what part of the implementation stumped you?
- If you had another week to work on this project, what would you add to your nifty store?
- What did you enjoy the most about this project? What was the most rewarding?
- Was the breakdown and checkpoints throughout the assignment helpful? Would you change how the assignment is broken down/what is due?

You can answer all of these questions, some of them or none. What we care about most is that you are reflecting on your experiences working on a full-stack project and evaluating your successes/failures along the way. You will submit this reflection on canvas.
