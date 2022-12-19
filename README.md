# AlexaGoogleGPT-RaspberryPiCompatible
A different kind of Alexa which uses GPT-3 to answer, I'm sure that in a no longer future this would be in every home (in my case is just a kind of DEMO). 
Using key word "Alexa" to record the question and key word "Blueberry" to get the answer. Examples of use below.

![DALL·E 2022-12-19 17 59 57 - Alexa AI, CPU, Digital art (1)](https://user-images.githubusercontent.com/73484962/208480464-7f7f630b-7a8b-436e-a50c-619728e5cfdd.png)

<h2>References</h2>

- Key words: [Porcupine](https://github.com/Picovoice/porcupine/tree/master/demo/python#accesskey)
- Audio recording: [PyAudio](https://pypi.org/project/PyAudio/)
- Speech to text: [Google Speech to Text API](https://cloud.google.com/speech-to-text/?utm_source=google&utm_medium=cpc&utm_campaign=emea-es-all-en-dr-bkws-all-all-trial-e-gcp-1011340&utm_content=text-ad-none-any-DEV_c-CRE_539593778341-ADGP_Hybrid%20%7C%20BKWS%20-%20EXA%20%7C%20Txt%20~%20AI%20%26%20ML%20~%20Speech-to-Text%2320-KWID_43700073026907112-aud-606988877934%3Akwd-298238406956-userloc_9047045&utm_term=KW_google%20voice%20to%20text%20api-NET_g-PLAC_&gclid=Cj0KCQiAtICdBhCLARIsALUBFcF3bWsI_5zyT2tD2j-_zIxZ6W-8IxMC0souQzqfFAZ64gJj-1Ch1ywaAswZEALw_wcB&gclsrc=aw.ds)
- Text to speech: [gtts](https://pypi.org/project/gTTS/)
- Intelligent answer: [Open AI API](https://openai.com/blog/openai-api/)
- Audio player: [PyGame](https://www.pygame.org/news)

<h2>Installing and preparing</h2>

1. Install Raspberry Pi OS in SD card
2. Install  Open AI API in Python<code>sudo pip3 install openai</code>
3. Install PyAudio in python <code>sudo pip3 install PyAudio</code>
4. Install Google Speech to Text API in python <code>sudo pip3 install google-cloud-speech</code>
5. Install gtts in python <code>sudo pip3 install gtts</code>
6. Install PyGame in python <code>sudo pip3 install PyGame</code>
7. Install Picovoice porcupine Python demo <code>sudo pip3 install pvporcupinedemo</code>
8. Create a new account on the Picovoice console and create a new access key, as described here: https://github.com/Picovoice/porcupine/tree/master/demo/python#accesskey
9. Follow this video to get your own Google speech to Text API key: https://www.youtube.com/watch?v=DtlJH6MgBso (save it as key.json in your repository folder)
10. Get your own Open AI API key here: https://openai.com/blog/openai-api/
   <pre>
   $ cd /usr/local/lib/python3.7/dist-packages/pvporcupinedemo/
   $ sudo rm -rf porcupine_demo_mic.py
   $ sudo wget https://raw.githubusercontent.com/Kalomano/AlexaGoogleGPT-RaspberryPiCompatible/main/porcupine_demo_mic.py
   </pre>
11. Inside the <code>porcupine_demo_mic.py</code> file in this repository, insert your own Open AI key, line 126
12. Inside the new <code>porcupine_demo_mic.py</code> file in this repository, insert your own repository path where your repository is (for example "/home/kalomano/Documents/AlexaGoogleGPT-RaspberryPiCompatible/"), don't forget to include the last and first "/", line 120
13. Replace the file <code>porcupine_demo_mic.py</code> with the file with the same name in this repository (changed by steps 11 and 12).

<h2>Run AlexaGPT</h2>

Run <code>porcupine_demo_mic --access_key *YourOwnPorcupineAccessKey* --keywords alexa blueberry
 </code> in your terminal
 
 Say **Alexa** to start recording your question, say **Blueberry** to stop recording and get your answer.
 
 <h2>Examples (tested on Raspberry Pi 3 model B)</h2>
 
 
