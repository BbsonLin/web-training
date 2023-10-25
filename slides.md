---
layout: cover
highlighter: shiki
css: unocss
colorSchema: dark
transition: fade-out
---

# Web Tech Introduction Ⅰ
Bobson Lin

---
layout: full
---

# History of Web

<img src="/history_of_web.svg" />

<div class="absolute left-24 top-50 z-1" v-click> 
    <ul>
        <li>Static Web Pages</li>
        <li>Mostly Read Only Web</li>
        <li>Information Sharing</li>
    </ul>
</div>

<div class="absolute left-63 top-53 w-40rem h-5rem bg-[#121212]"></div>

<div class="absolute left-145 top-78 w-20rem h-5rem bg-[#121212]"></div>


---
layout: full
---

# History of Web - Web 1.0
1990 - 2004


<div class="grid grid-cols-[320px_1fr] gap-4">
    <div>
        <img src="/ie.jpg" class="w-16rem" />
        <ul>
            <li>Ecommerce</li>
            <li>Search Engine</li>
        </ul>
    </div>
    <div>
        <img src="/nasa-1997.jpeg" />
    </div>
</div>

<!-- 
Ecommerce: Amazon, Ebay  ...
Search Engine: Google, Yahoo ...
 -->


---
layout: full
---

# History of Web

<img src="/history_of_web.svg" />

<!-- <div class="absolute left-63 top-53 w-40rem h-5rem bg-[#121212]" v-click-hide="1"></div> -->

<div class="absolute left-65 top-73 z-1" v-click="1"> 
    <ul>
        <li>Dynamic Web Pages</li>
        <li>Read-Write Web</li>
        <li>Information Sharing</li>
    </ul>
</div>

<!-- <div class="absolute left-145 top-78 w-20rem h-5rem bg-[#121212]" v-click-hide="3"></div> -->

---
layout: full
---

# History of Web - Web 2.0
2000 - Now


<div class="grid grid-cols-[320px_1fr] gap-4">
    <div class="flex flex-justify-center items-center flex-col">
        <img src="/chrome.png" class="w-10rem" />
        <ul>
            <li>SaaS</li>
            <li>Social Media</li>
            <li>Streaming Media</li>
        </ul>
    </div>
    <div class="flex flex-justify-center items-center flex-col">
        <img src="/SaaS.svg" class="w-12rem" />
        <img src="/SocialMedia.svg" class="w-12rem" />
        <img src="/StreamingMedia.svg" class="w-12rem" />
    </div>
</div>



::right::

* SaaS
* Social Media
* Streaming Media



<!-- 
SaaS: Google Apps (Gmail, Google Drive) ...
Social Media: Facebook, Twitter, Instagram ...
Streaming Media: Youtube, Netflix ...
 -->


---
layout: full
---

# Web 2.0
Web Application

<div class="grid grid-cols-[1fr_100px_1fr] gap-4">
    <div class="flex flex-justify-center items-center flex-col">
        <div>Frontend</div>
        <img src="/web_frontend_rmbg.png" class="w-20rem mt-3rem" />
    </div>
    <div class="flex flex-justify-start flex-col">
        <div class="absolute left-110 top-50">HTTP / HTTPS</div>
        <Arrow x1="450" y1="240" x2="550" y2="240" />
        <Arrow x1="550" y1="280" x2="450" y2="280" />
        <Arrow x1="450" y1="380" x2="550" y2="380" />
        <Arrow x1="550" y1="380" x2="450" y2="380" />
        <div class="absolute left-113 top-85">WS / WSS</div>
    </div>
    <div class="flex flex-justify-center items-center flex-col">
        <div>Backend</div>
        <img src="/server.png" class="w-10rem mt-3rem" />
    </div>
</div>
<div class="flex flex-justify-center mt-3rem">Web APIs</div>


---
layout: full
---

# Web Backend
Web Server


* Deliver static content.
* Content is delivered using the HTTP protocol only.
* Serves only web-based applications.


<div class="grid grid-cols-2 gap-4">
    <div class="flex flex-justify-start items-center flex-col">
        <img src="/Web_Server.jpeg" class="w-30rem mt-2rem" />
    </div>
    <div class="flex flex-justify-start items-center flex-col">
        <img src="/Web_servers_logo.svg" class="w-24rem" />
    </div>
</div>

<!-- https://www.educative.io/answers/web-server-vs-application-server -->

---
layout: full
---

# Web Backend
Application Server

* Delivers dynamic content.
* Provides business logic to application programs using several protocols (including HTTP).
* Can serve web and enterprise-based applications.

<div class="grid grid-cols-2 gap-4">
    <div class="flex flex-justify-start items-center flex-col">
        <img src="/Application_Server.jpeg" class="w-30rem mt-1rem" />
    </div>
    <div class="flex flex-justify-start items-center flex-col">
        <img src="/MPA_framework.svg" class="w-20rem mt-1rem" />
        <div>Web Frameworks</div>
    </div>
</div>


<!-- https://www.educative.io/answers/web-server-vs-application-server -->

---
layout: full
---

# Web Frontend
Web App

<div class="grid grid-cols-2 gap-4">
    <div class="flex flex-justify-start items-center flex-col">
        <div class="text-3xl">MPA</div>
        <img src="/MPA.jpg" class="w-30rem mt-1rem" />
    </div>
    <div class="flex flex-justify-start items-center flex-col">
        <div class="text-3xl">SPA</div>
        <img src="/SPA.jpg" class="w-30rem mt-1rem" />
    </div>
</div>


---
layout: full
---

# Web Frontend
Web App

<div class="grid grid-cols-2 gap-4">
    <div class="flex flex-justify-start items-center flex-col">
        <div class="text-3xl">MPA</div>
        <img src="/MPA_pros_cons.jpg" class="w-16rem mt-1rem" />
        <img src="/MPA_framework.svg" class="w-20rem mt-1rem" />
    </div>
    <div class="flex flex-justify-start items-center flex-col">
        <div class="text-3xl">SPA</div>
        <img src="/SPA_pros_cons.jpg" class="w-16rem mt-1rem" />
        <img src="/SPA_framework.svg" class="w-20rem mt-1rem" />
    </div>
</div>


---
layout: full
---

# Real World Project
SDAQ & EMU

