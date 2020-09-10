# GroupProject_StayHome_API
This is the **main project Readme**, for UI code, visit:<br>https://github.ccs.neu.edu/NEU-CS5610-SU20/GroupProject_StayHome_UI

## Team Info
TeamName: StayHome       
App Name: Teatime music website     
Team Member: Chuanyang Tang, Nan Ke   

## Heroku Application
https://stayhome-ui.herokuapp.com

## A Brief Introduction of this site
[User guide](./Intro.md)

## Run in localhost
* Clone API repo and install dependency:
  ```
  npm install
  npm start
  ```
* Clone UI repo and install dependency, configure `.env` file
  ```
  npm install

  # comment this line in .env
  REACT_APP_API_ENDPOINT=https://stayhome-api.herokuapp.com/graphql

  npm start
  ```
The streaming service might not be reliable due to the restriction of heroku, we recommend test on localhost to get better experience.

## Iter 3 - StayHome
* Progress
  * Added responsive design for music player and all pages
  * Created user info edit function
  * Used react bootstrap alert and tooltips
  * Implemented a music search page to show results from youtube which can be play on our player
  * Used reCAPTCHA to test if the user is a robot when register
  * Added player toggle button 
  * Added username password email format verification when register

* Contributions
  * Nan Ke   
      - Added responsive design for music player
	  - Added react boostrap alert  
	  - Implemented a music search page to show results from youtube which can be play on our player
    - Used reCAPTCHA to test if the user is a robot when register 
    - Added player toggle button to show or hide the player
  * Chuanyang Tang
    - Added responsive design for all pages
	- Implemented user info edit function
	- Added react bootstrap tooltips
  - Added username password email format verification when register

  * Screenshots
  1. mainpage
  ![image](readme_images/iter3/mainpage.jpg)
  2. myhomepage
  ![image](readme_images/iter3/myhome.jpg)
  3. music search results
  ![image](readme_images/iter3/musicsearch.jpg)
  4. music info page
  ![image](readme_images/iter3/musicinfo.jpg)
  5. register modal and format verification
  ![image](readme_images/iter3/register.jpg)
  6. responsive design
  ![image](readme_images/iter3/responsive1.jpg)
  ![image](readme_images/iter3/responsive2.jpg)
  7. search music link<br>
  ![image](readme_images/iter3/searchMusicLink.gif)
  8. search keywords<br>
  ![image](readme_images/iter3/searchKeywords.gif)
  9. edit user info<br>
  ![image](readme_images/iter3/editUserInfo.gif)
  10. add and delete playlist<br>
  ![image](readme_images/iter3/addDeletePlaylist.gif)
  11. show and hide player in small screen<br>
  ![image](readme_images/iter3/showHidePlayer.gif)

## Iter 2 - StayHome
* Progress
  * Deployed api and ui on heroku respectively
  * API
    * Connected to MongoDB Atlas cloud database
    * Implemented graphql authentication (JWT token based)
    * Finished GraphQL schema and resolver
  * UI
    * Feature update: login, register, addplaylist, deleteplaylist, addmusic, deletemusic  
    * bugs fixed: added callback for play() promise rejection, support login modal autocomplete
    * styled player, myhome page

* Contributions
  * Nan Ke   
      - Implemented authentication on backend
	  - Refactor and bug fixed a music player   
	  - Feature update for player, login, register    
  * Chuanyang Tang
    - Feature update: addplaylist, deleteplaylist, addmusic, deletemusic  
	- styled myhome page
	- Config MongoDB Atlas cloud database

* Screenshots
  1. mainpage
  ![image](readme_images/iter2/Mainpage.png)
  2. myhomepage
  ![image](readme_images/iter2/MyHomePage.png)
  3. playlist details
  ![image](readme_images/iter2/PlaylistDetails.png)
  4. add playlist
  ![image](readme_images/iter2/AddPlaylist.png)




## Iter 1 - StayHome
* Progress
	* Created front end and back end repos and they can be working together
	* Created React components to represent CRUD functionality like playing music, displaying user’s basic information and so on
	* Designed GraphQL schema for CRUD operations
	* Added routers, links to connect different pages
	* Used `ytdl-core` package to get music stream and information from Youtube
	* Implemented a html5 `<audio>` tag based music player
	* Used `react-bootstrap` to make our web look professionally styled and responsive

* Contributions
  * Nan Ke   
      - search music and get its stream from Youtube    
	  - implemented a music player which has play, pause, next, pre and shuffle functions       
	  - implemented musicInfo page    
  * Chuanyang Tang
    - get user info and display in myhome page
	- implemented navigation, myhome, main components
	- designed GraphQL schema and added routers

* Screenshots
  1. mainpage
  ![image](readme_images/mainpage.jpg)
  2. login
  ![image](readme_images/login.jpg)
  3. register
  ![image](readme_images/register.jpg)
  4. musicinfo
  ![image](readme_images/musicinfo.jpg)
  5. playlist
  ![image](readme_images/playlist.jpg)
  6. myhomepage
  ![image](readme_images/myhomepage.jpg)


## Notes:
* GraphQL query/mutation
  * All GraphQL operations are written in `GraphQL.md`

* Bugs:
  * The stream server might crash due to set header after response is sent out. Try to setup callback/.then() but no luck -- **resolved**


## Important Change Log:
* 3rd Aug, schema updated for signup/signin:
  * Removed address/phone
  * userInput -> signupInput
  * Added signup/login Mutation
