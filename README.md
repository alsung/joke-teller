# Joke Teller
JS Web Project Joke Teller\
View Here: https://alsung.github.io/joke-teller/

## About
The goal of this project is to implement a joke telling app that uses a joke API to fetch jokes and feeds that data to a text-to-speech API to say the joke out loud. A button is present on the application, and upon pressing the button, the application fetches a new joke from the joke API, transforms the joke into a string to be passed as the source to the text-to-speech API. 

## Built With

### Front End
 - HTML5
 - CSS
 - JavaScript

### APIs
 - Joke API
 - VoiceRSS Text-to-Speech API

## Functionality
In my JavaScript file, the getJokes() method fetches a joke from json data from the joke API. The joke API responds with either a one part 'joke' or a two part joke with a 'setup' and 'delivery'. If there is both a 'setup' and 'delivery', then we combine both components into a single string separated by ellipses. Otherwise, we store the joke as a string variable to be passed to the VoiceRSS API. 

Passing the joke string variable to the VoiceRSS API, the method will trigger the VoiceRSS Javascript SDK which will return the audio data for the joke string variable passed in. When the audio source data is returned, we pass that to the source of our audio element, and play the audio, thus allowing the user to hear the joke aloud. 
![Figure 1](/images/joke_teller_flowchart.png)

## Resources
 - https://sv443.net/jokeapi/v2/: Joke API
 - http://www.voicerss.org/api/: VoiceRSS API

## Contributors
 - [**Alexander Sung**](https://github.com/alsung) - Creator