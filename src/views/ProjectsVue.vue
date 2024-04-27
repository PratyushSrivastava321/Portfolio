<template>
    <v-container>
      <v-card style="padding: 20px" color="#0B0A12" elevation="3">
        <div v-for="(item, index) in components" :key="index">
          <v-row>
            <v-col cols="24" md="12">
              <v-card color="#0B0A12" class="box text-center card-hover-effect" elevation="12">
                <v-card-text>
                  <div class="text-container">
                    <h6>{{ item.duration }}</h6>
                    <h4 style='font-family: "Montserrat";color:#2fbf71'>{{ item.title }}</h4>
                    <h6>{{ item.techUsed }}</h6>
                    <h5>{{ item.about }}</h5>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-card>
    </v-container>
  </template>
  
  <script>
  export default {
    data(){
      return{
        components:[
          {techUsed:"Playwright",title:" Scrolller Image Scraper",duration:" March 2024 ",about: " A program which can scrape all the images present in a reddit subpage present on scrolller. It goes to the provided URL in a playwright window and checks for each api call for an image and gets that api call and puts that URL in a text file present in that folder and later when all the links of all the pictures present in that webpage are scraped another file is to be executed which will check for all the values in the links.txt file and download all the pictures and stores all the images in a particular folder. "},
          {techUsed:"Arduino",title:" Motion Sensor Security Camera with Notification using Blynk IoT Project ",duration:" January 2023 ",about: " This was an IoT project made given by college. In this project we had to make a doorbell which had an ESP32 cam attached to it alongwith a microcontroller NodeMCU ESP8266 .It will send an image via Blynk to the user if someone pressed the doorbell . Now if the user authorizes the person at the door a request is sent to door lock which will unlock the solenoid lock."},
          {techUsed:"Console Based",title:" Wordle + Solver ",duration:" October 2022 ",about: "Wordle is a famous game where player has to guess a 5 letter word where he is provided with 6 tries. I created by gathering all the 5 letter words from the english_word_set module and then used random() to chose a random word given in the set. Now for its solver I first tried any word which had all the distinct letters, then if any letter turns out to be yellow we check words only which have those yellow letters and if letter turns out to be green we will only use the words which have that letter in that position only. "},
          {techUsed:"Selenium",title:" Monkeytype (website) auto typing bot ",duration:" September 2022 ",about: " Monkeytype.com is a famous website which allows users to take a typing test to check their typing speed by giving them 30s and a text paragraph to type and speed is calculated by no.of words you typed in given no of seconds. If time is 30s your score will be twiced or if it is 15s your score will be quadrupled. Now what I did was to open a browser with selenium and goto that URL and click some buttons by their Xpath and then extracted the innerHTML of a particular span tag of whatever is to be typed. Now pyautogui provides the functionality to enter keys and with that we simply type the whole paragraph."},
          {techUsed:"Logging",title:" Keylogger ",duration:" August 2022 ",about: " This keylogger was basically a log of whatever input is given from the keyboard and that input was stored it inside a notepad. It was executed with a bash script which automatically starts this keylogger whenever the computer is switched on "},
          {techUsed:"Themed Tkinter (TTK) ",title:" WPM Calculator(Typing Test) ",duration:" November 2021 ",about: " A WPM(Words per minute) Calculator which determines your typing speed. Here user is provided with some of the most famous and iconic lines from movies and is told to write them as quickly as possible. After the user starts to write we start a timer and that timer stops when the user finishes the text, then we will calculate the speed of the user with the formula of (No. of words)/(time used)"},
          {techUsed:"Tkinter",title:" Tic Tac Toe GUI ",duration:" April 2020 ",about: " Made a Tic Tac Toe GUI where 2 users can play it simultaneously. It is a GUI app where we divide the screen into 9 equal squares and check where the user has clicked and locate which square lies in it. If the square is not taken user can put his value there"},
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  span{
    color : #2fbf71;
  }
  .box h5 {
    font-size: 14px;
    font-weight: 500;
    color: var(--2nd-main-color);
  }
  .box p {
    font-size: 1em;
    font-weight: 300;
    margin-bottom: 1.2rem;
    line-height: 1.8rem;
    color: #ffffffcc;
  }
  .box h6{
    color: #3e4455;
    font-size: 14px;
    font-weight: 600;
    margin-bottom: 10px;
  }
  .box{
    padding: 15px;
  }
  .box h4 {
    color: #fff;
    font-size: 1.3rem;
    font-weight: 700;
    margin-top: 10px;
    margin-bottom: 13px;
  }
  .card-hover-effect {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .card-hover-effect:hover {
    transform: translateY(-5px) translateX(-5px);
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  }
  </style>
  