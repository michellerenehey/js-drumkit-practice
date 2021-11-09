# js-drumkit-practice
JS 30 - day 1!

## HTML 
- We will start with a div container, with a class of "keys". Inside that div container, we will have 9 child divs - representing each of the 9 keys that will makeup our drumkit (A, S, D, F, G, H, J, K, L). Each div will have two pieces of code in it: a grandchild KBD (keyboard input element - which holds the name of the key: a, s, d, f....) and a grandchild span (which will hold the name of the sound: hihat, kick, openhat...)
- container div: class="key"
- each child div: data-key="*key number*", class="key"
- each kbd grandchild stands alone
- each span grandchild has class="sound"

- we will also grab all 9 audio elements in the html. these will share data-keys with the child divs above, and grab sound from assets.

## JS
- logic: 
    - add a keydown event listener for each of the 9 keys. on the event (kedown) run a function: 
        - play a sound: 
            - grab the audio for the particular key that was keyed down (document.querySelector(`audio[data-key="${e.keyDown}"]`), and audio.play(). 
            - add "if no audio, stop the function" 
            - add "audio.currentTime = 0" so that the sound can keep playing
        - add animation to the key: 
            - grab the class of "key" for the particular key that was keyed down (document.querySelector(`.key[data-key="${e.keyDown}"]`), and add a class of "playing". 
            - loop through each key, listen for when the transition-end happens, and add a "transition end" event that will fire when the animation stops


## CSS
- going to use the CSS built for me by Wes, but will re-write it line by line so that I understand 