![[Pasted image 20250215233847.png]]

##### through every request we make we are essentially downloading html css and js files.
as all of the sites in web use these 3 primarly.

![[Pasted image 20250215234012.png]]

![[Pasted image 20250215234022.png]]

basic framework of how things work in web surfing.

![[Pasted image 20250216002201.png]]

#### dynamically made websites
A **Single-Page Application (SPA)** is a web application that loads a **single HTML page** and dynamically updates content using **JavaScript**, instead of reloading the page for each interaction. This creates a **fast and smooth user experience**, similar to native apps.

So if we check the source page of these sites it'll give us a very short html which doesnt look like it has any elements that are present in site 
thus js is being used to render everything.

can also check through network tab in the inspector tool , if a lot of communication is there and alot of js is being updated then yeah it is SPA.

##### to tackle this problem (as when scraping the html wont be used in a simple manner)
we use headless browsers.
