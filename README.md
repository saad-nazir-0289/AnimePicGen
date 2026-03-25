# Neko Image Generator

A simple and fun web project that fetches random anime catgirl images using the **Nekos API** and displays them instantly in the browser.

This project is built with:

* **HTML**
* **CSS**
* **JavaScript**

It is a beginner-friendly mini project that demonstrates how to:

* fetch data from a public API
* work with asynchronous JavaScript
* update the DOM dynamically
* create an interactive UI with a button click

---

## Preview

The app shows:

* a random **neko image** when the page loads
* a **button** to fetch another random image
* a clean and simple frontend built using HTML and CSS

---

## Features

* Random anime neko image generator
* Fetches live images from an external API
* Auto-loads one image on page open
* Button to generate a new image instantly
* Beginner-friendly and lightweight project

---

## Technologies Used

* **HTML5** for structure
* **CSS3** for styling
* **JavaScript (ES6)** for logic and API handling
* **Nekos API** for image data

---

## How It Works

The JavaScript does the following:

1. Sends a request to the API:

   ```js
   https://nekos.best/api/v2/neko
   ```

2. Receives JSON data from the API

3. Extracts the image URL from:

   ```js
   data.results[0].url
   ```

4. Sets the image source dynamically:

   ```js
   img.src = firstresult;
   ```

5. Displays a new image every time the button is clicked

---

## Project Structure

```bash
Neko-Image-Generator/
│── index.html
│── style.css
│── script.js
│── README.md
```

---

## JavaScript Logic

Main functionality used in the project:

* **`fetch()`** to call the API
* **`async / await`** for asynchronous handling
* **DOM manipulation** to update the image
* **Event Listener** to generate new images on button click

Example logic:

```js
const URL = "https://nekos.best/api/v2/neko";
let img = document.querySelector("#happy");
let btn = document.querySelector("#btn");

const getfacts = async () => {
  console.log("Getting Data....");
  let response = await fetch(URL);
  let data = await response.json();
  const firstresult = data.results[0].url;
  img.src = firstresult;
  img.style.display = "block";
};

getfacts();
btn.addEventListener("click", getfacts);
```

---

## How to Run the Project

### Option 1 — Open Directly

Just open the `index.html` file in your browser.

### Option 2 — Use Live Server (Recommended)

If you're using **VS Code**:

1. Install the **Live Server** extension
2. Right-click on `index.html`
3. Click **Open with Live Server**

---

## Learning Concepts Covered

This project is useful for beginners learning:

* JavaScript API calls
* Async programming
* JSON handling
* DOM selection and manipulation
* Event handling
* Frontend mini project structure

---

## Future Improvements

Possible upgrades you can add later:

* Loading spinner while fetching images
* Error handling if API fails
* Download image button
* Category switcher for different anime image types
* Better animations and UI styling
* Save favorite images feature

---

## Why This Project Is Good for Beginners

Because it teaches one of the most important frontend concepts:

> How to connect your website with a real API and show dynamic content on screen.

That is the foundation of most modern web apps.

---

## Credits

Image source powered by:

* **Nekos API** → https://nekos.best/

---

## Author

Made as a fun frontend practice project using **HTML, CSS, and JavaScript**.
