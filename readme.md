# Club Website Creation 

The website is built with Hugo. 

## Creating a site for your club  

1. Go to the `content` folder and create a folder for your club. 
2. A sample club has been given, so copy all the files in that sample club to the newly created folder.
3. In every `_index.md` change the `type: club_name/` to one `type:your_Club_name/`
4. Go back to the root directory
5. Now go to `layouts` folder,
6. Cooy the sample folder given.
7. Rename it to be your club name. 

1. Cd into the content folder and copy the sample `club_name` folder. 
2. Rename it to the desired name. The path reach your clubs website now is `localhost:xxxx/clubs/club_name`. (xxx is your port number on the local machine. Typcially it is 1313 for this.)
3. `grep -r club_name` in the content directory and change every instance of it in your folder to that of your folder name

1. Go back to the root.
2. cd into `data` and copy the sample `club_name` folder.
3. Rename it to the same folder name you gaver earlier for content
4. `grep -r club_name` in the data directory and change every instance of it in your folder to that of your folder name
5. `team.yml` contains the memebers of the club, modify it accordingly.
6. `activities.yml` contains the list of major events your club does and gets listed in the homepage of your club. 
7. `event.yml` shows a list of events conducted and gets displayed as a gallery, on the events page. 
5. Modify the `title` and `type` in `event.yml` to reflect the events in `activities.yml`.


1. Go back to root. 
2. cd into `layouts` and copy the sample `club_name` folder.
3. `grep -r club_name` in the content directory and change every instance of it in your folder to that of your folder name

## Deploying the site on the local machine 

1. We use, `Hugo` a static site generater to generate the website. 
2. Install [Hugo](https://gohugo.io/getting-started/installing/) 
3. Install the theme, instructions available [here](https://github.com/themefisher/kross-hugo). 
4. Run `hugo server` to run the server on your local machine. Execute this command in the root directory of the project. 
5. If you have drafts, then run `hugo server -D` to view them. Do not keep drafts, and set the value to `False` when you're done as they do not get deployed on the site. 

## Adding Content 

1. Run `hugo new event_name.md` in the `/content/your-club-name/archive`. 
2. All the content posts are written in Markdown, and you can look into the Hugo Documentation for more details.
3. Modify the `event.yl` file in the `/data/your-club-name/`, and add a picture for that event. 
4. Make a new entry directly below the old ones, and give it a picture, and link it to the event-post created in the archive section done earlier. You can do a hardlink if you want(site is deployed on www.clubs.iiit.ac.in/clubs/your-club-name), but preferably make it a relative link, with the link being `{{< ref "/your-club-name/archive/my-post" >}}`.
5. Add the relavant `type` for it. 
6. If you want to add more than one picture make a seperate entry in `activities,yml


## Adding events to your club 

1. Take a look at data. 

