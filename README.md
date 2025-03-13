# Drop & Heal
Drop & Heal is a web application designed to support young adults in processing grief. The application analyzes the user’s current grief stage and assigns them to a specific grief task. Based on this analysis, tailored exercises are provided to help them cope with their loss.
This project is built using Node.js and Express.js for the backend, LiquidJS as a template engine, and Directus API for dynamically retrieving and displaying content.

## Inhoudsopgave

  * [Goal](#goal)
  * [Technologies](#technologies)
  * [Achievements](#achievements)
  * [Live-Version](#live-version)

## Goal

The goal of Drop & Heal is to create a user-friendly, responsive, and intuitive web application that:

Dynamically retrieves data from an external database via Directus API.
Displays grief tasks and exercises based on an automated user analysis.
Uses server-side rendering with Node.js and Express.js.
Implements LiquidJS templates to generate dynamic HTML pages.
Provides an empathetic and accessible interface for young adults at different stages of rouwtaak.


## Technologies
This project utilizes the following technologies:

Node.js	JavaScript runtime for backend functionality
Express.js	Web framework for routing and API communication
LiquidJS	Template engine for dynamic HTML rendering
Directus API	CMS storing exercises and grief tasks
Fetch API	Retrieves and processes data from Directus

## 1.API Calls in Express
To call and fetch task and exercises from Directus:
https://github.com/yamenAl/server-side-rendering-server-side-website/blob/6426a6dbf7949ca3dff9fd5d82f43b6caa41af12/server.js#L9-L23

## 2.Filtering Data in Express
filtering directly in the API request:
https://github.com/yamenAl/server-side-rendering-server-side-website/blob/6426a6dbf7949ca3dff9fd5d82f43b6caa41af12/server.js#L11-L13


## 3.Passing Data to LiquidJS
The retrieved data is passed to LiquidJS templates for rendering:
<br>
First here the index 
https://github.com/yamenAl/server-side-rendering-server-side-website/blob/6426a6dbf7949ca3dff9fd5d82f43b6caa41af12/server.js#L59-L70

Here passed data to rouwtaak page
https://github.com/yamenAl/server-side-rendering-server-side-website/blob/6426a6dbf7949ca3dff9fd5d82f43b6caa41af12/server.js#L84-L97

## 4.How LiquidJS Uses Data
LiquidJS is the template engine that dynamically generates HTML pages with the retrieved data.

Displaying a List of Exercises and exerciese data as object.
https://github.com/yamenAl/server-side-rendering-server-side-website/blob/6426a6dbf7949ca3dff9fd5d82f43b6caa41af12/views/het-verlies-aanvaarden.liquid#L26-L33

This loops through all exercises and displays the title, description.

## 4.Highlighting a Specific Exercise
A single featured exercise can be displayed as object:
https://github.com/yamenAl/server-side-rendering-server-side-website/blob/6426a6dbf7949ca3dff9fd5d82f43b6caa41af12/views/index.liquid#L16C8-L23C37
<br>

## 5.Redirects and 404 Handling
To properly handle incorrect URLs, a redirect system are implemented.

https://github.com/yamenAl/server-side-rendering-server-side-website/blob/ca7558faa63cdbc50ca88369e764cc8b1023a3cf/server.js#L118-L121

This ensures that when a user enters an invalid link, they are redirected to a custom error page.



## Achievements
Loaded tasks and exercises data dynamically on both the index page and the grief task (rouwtaak) page.
1.Fetched and displayed exercises based on the selected rouwtaak using Express.js and LiquidJS.
2.Implemented filtering to ensure users only see exercises relevant to their rouwtaak task id.
3.Optimized API calls to retrieve only necessary data, improving performance.
## Home page.
![home-page](https://github.com/user-attachments/assets/5405dc99-1d55-4a73-be12-2f7d19ab7de9)
## Rouwtaak page.
![rouwtaak-page](https://github.com/user-attachments/assets/189c3f76-c5c2-4210-a467-b0085f402b7f)

## Live-Version
Check out the live website here
[Drop & Heal](https://server-side-rendering-server-side-website-7pwt.onrender.com)


## Bronnen
[docs/INSTRUCTIONS.md](docs/INSTRUCTIONS.md)
## Licentie

This project is licensed under the terms of the [MIT license](./LICENSE).
