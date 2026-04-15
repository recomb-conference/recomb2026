---
layout: home
title: RECOMB 2026
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RECOMB 2026 Pop-Up</title>
    <style>
        .popup {
            display: none;
		    position: fixed;            /* stay relative to the viewport */
		    top: 200px;                  /* distance from top */
		    left: 50%;                  /* move to horizontal center */
		    transform: translateX(-50%); /* true centering */
		    width: 40%;
		    max-width: 900px;
		    height: auto;
		    max-height: 80vh;
		    overflow-y: auto;
		    background-color: #ffffff;
		    z-index: 1100;
		    border: 2px solid #ddd;     /* nice visible border */
		    border-radius: 10px;        /* smooth corners */
		    box-shadow: 0 10px 30px rgba(0,0,0,0.2); /* floating effect */
		    padding: 10px;
        }
        .popup-content {
            position: relative;
            width: 100%;
			height: auto;
            max-width: 600px; /* Adjusted for image size */
            margin: 5% auto; /* Centered with less top margin for image */
            padding: 10px;
            border-radius: 5px;
            text-align: center;
        }
        .popup-content img {
            width: 100%;
            height: auto;
            border-radius: 5px;
        }
        .close-btn {
            position: absolute;
            top: 5px;
            right: 5px;
            font-size: 22px;
			font-weight: bold;
            cursor: pointer;
            color: #000;
            background: #fff;
            width: 25px;
            height: 25px;
            line-height: 20px;
            text-align: center;
            z-index: 10;
        }
        .checkbox-label {
            font-size: 14px;
            margin-top: 10px;
            display: block;
        }
        
    </style>
</head>

<body>
    <div id="myPopup" class="popup">
		<span class="close-btn" onclick="closePopup(event)">×</span>
        <div class="popup-content">
            <div style="position: relative;">
				<center>
					<h2>Visa Requirements</h2>
				</center>
                <p style="text-align:justify">
              All participants should verify their visa requirements prior to attending the conference. Requirements vary by citizenship and passport type. <br><br>
              For official information, please consult the <a href="https://www.mfa.gr/en/services/visas-for-foreigners-traveling-to-greece/countries-requiring-or-not-requiring-a-visa/" target="_blank">Hellenic Republic Ministry of Foreign Affairs</a> website to check if your country requires a visa. 
					<br><br><b>Please note that you must complete registration to be able to obtain a visa support letter</b>.</p>
                <div style="text-align: center; margin-top: 2rem;">
                  <a href="https://transition.iscb.org/cms_addon/conferences/recomb2026/easychair/visa"
                     style="
                       display: inline-block;
                       padding: 12px 28px;
                       font-size: 16px;
                       font-weight: 600;
                       color: #ffffff;
                       background-color: #000000;
                       text-decoration: none;
                       border-radius: 6px;
                     "
                     target="_blank">
                    Click here to get your visa invitation letter.
                  </a>
                </div>
                <br>
            </div>
            <label class="checkbox-label">
                <input type="checkbox" id="dontShowOneDay" onclick="setCookie(); event.stopPropagation();">
                Don’t show this pop-up again today
            </label>
        </div>
    </div>
    <script>
        // Function to set a cookie for 1 day
        function setCookie() {
	    let dontShow = document.getElementById("dontShowOneDay").checked;
            if (dontShow) {
                let date = new Date();
                date.setTime(date.getTime() + (24 * 60 * 60 * 1000)); // 1 day
                document.cookie = "popupDismissed=true; expires=" + date.toUTCString() + "; path=/";
            } else {
                // If unchecked, set a cookie with a past expiration to "delete" it
                document.cookie = "popupDismissed=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/";
            }
        }
        // Function to check if cookie exists
        function getCookie(name) {
            let value = "; " + document.cookie;
            let parts = value.split("; " + name + "=");
            if (parts.length === 2) return parts.pop().split(";").shift();
        }
        // Function to open the pop-up
        function openPopup() {
            document.getElementById("myPopup").style.display = "block";
        }
	// Function to close the pop-up and set cookie based on checkbox
        function closePopup() {
            setCookie(); // Set cookie based on checkbox state when closing
            document.getElementById("myPopup").style.display = "none";
        }
        // Open pop-up on page load if cookie not set
        window.onload = function() {
            if (!getCookie("popupDismissed")) {
                openPopup();
            }
        };
    </script>
  </body>

<center>
<h1>About {{ site.title }} & H.bioinfo'17</h1> 
</center>

---
### {{ site.iteration }} Annual International Conference on Research in Computational Molecular Biology

{{ site.title }} is the {{ site.iteration }} edition of a series of algorithmic computational biology conferences bridging the areas of computational, mathematical, statistical and biological sciences. The conference features keynote talks by preeminent scientists in life sciences, presentations of ground breaking research in computational biology, selected over the course of a highly-rigorous peer-review process, and poster sessions on the latest research progress. 

---
### Joint Events: {{ site.title }} and H.bioinfo'17 in Thessaloniki

The H.bioinfo conference series brings together bioinformatics experts, computational biologists, computer scientists and engineers, as well as researchers from related disciplines including biology, physics, chemistry, mathematics, statistics, epidemiology, clinical sciences, and pharmacology, to serve the broader community’s needs for education, training, and networking.

Under the auspices of the Hellenic Bioinformatics Society, in affiliation with the International Society for Computational Biology, and hosted by the Aristotle University of Thessaloniki, RECOMB 2026 and H.bioinfo'17 will be held jointly in Thessaloniki, Greece, at the Thessaloniki Concert Hall.

---
## Get in touch

### Contact details

- Email: [{{ site.author.email }}](mailto:{{ site.author.email }})
- X: [@RECOMBConf](https://x.com/RECOMBconf)
- Bluesky: [@RECOMBConf](https://bsky.app/profile/recombconf.bsky.social)
