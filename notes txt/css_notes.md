NOTES (Sec 4, Lec 31)

- Cascading Style Sheets, or CSS, is used to style and layout the visuals of a website.
- Commonly used in tandum with HTML files
- We are able to inject CSS right into the HTML tags (Usually the body tag)
- the "style=" attribute takes CSS code as an input parameter
- to know which css property to use, go to MDN. [background-color](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
- To help with color palettes, use [colorhunt.co](https://colorhunt.co/)

NOTES (Sec 4, Lec 32)

- In the previous notes, we styled the background of the webpage by injecting css code to the body element of the HTML file
  using the "style=" attribute
- To add style to the whole webpage, we can add a <style></style> tag within the <head> tag of the html file
- No webpage is unstyled, each webpage is rendered with a default css styling applied to it.
- When working with sizing of HTML elements, its important to be cautious when working with fixed heights and widths because it
  will effect the responsiveness of the webpage when the browser changes size.
- Be sure to view the [syntax](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#syntax) of new attributes to understand its full functionality.
- how can we create external CSS to style all our HTML files

NOTES (Sec 4, Lec 33)

- Create css files to apply external css across multiple HTML files
- Using the link element to tell the HTML file where to retrieve the stylesheets from, as opposed to the
  default stylesheet provided by most browsers and the internal style element we used earlier.
- It is important to remember to not use a "/" in your href when you are working on a static website. If so, than the
  href will look in the root files of the webpage, which only exist when the webpage is being hosted.
- apply the <link> element to all HTML files you wish to style.

NOTES (Sec 4, Lec 35)

- Original Code:
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <meta charset="UTF-8" />
      <title>Mahmoud's Personal Website</title>
      <link rel="stylesheet" href="css/styles.css" />
    </head>

    <!--<body style="background-color: #a3ddcb">-->
    <body>
      <table cellspacing="20px">
        <tr>
          <td>
            <img
              src="images/circle-cropped.png"
              alt="Mahmoud's Profile Picture"
            />
          </td>
          <td>
            <h1>Mahmoud Shabana</h1>
            <!-- <i>Graduate Student-Athlete at Monmouth University</i> -->
            <p>
              <em>
                Graduate Student-Athlete at
                <strong>
                  <a
                    href="https://monmouthhawks.com/sports/football/roster/mahmoud-shabana/10362"
                    >Monmouth University</a
                  >
                </strong>
              </em>
            </p>
            <p>
              I am a SE Graduate that also plays Division 1 football at Monmouth.
              I love to swim, travel, and read about all things technology! I am
              excited to become an expert in web stack development and hope to
              start my career off with a solid foundation.
            </p>
          </td>
        </tr>
      </table>

      <hr />
      <h3>Education:</h3>
      <ul>
        <li>
          <strong>
            <a href="https://www.monmouth.edu/"> Monmouth University </a>
          </strong>
        </li>
        <ul>
          <li>B.S in <em>Software Engineering</em> From 2016 - 2020</li>
          <li>
            M.S in <em>Software Engineering - Advanced Thesis Track</em> From 2020
            - 2021
          </li>
        </ul>
        <li>
          <strong>
            <a href="https://www.bths.edu/"> Brooklyn Technical High School </a>
          </strong>
        </li>
        <ul>
          <li>Focus in <em>Civil Engineering</em> From 2012 - 2016</li>
        </ul>
      </ul>
      <hr />
      <h3>Work Experience</h3>
      <table border="3px" cellspacing="5px">
        <colgroup span="4"></colgroup>
        <thead>
          <tr>
            <th>From</th>
            <th>To</th>
            <th>Position</th>
            <th>Employer</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><em>May 2019</em></td>
            <td><em>Aug 2019</em></td>
            <td>Software Developer Intern</td>
            <td>Wakefern Food Corp CIS Division</td>
          </tr>
          <tr>
            <td><em>May 2018</em></td>
            <td><em>Aug 2018</em></td>
            <td>Software Development Researcher</td>
            <td>Monmouth University School of Science</td>
          </tr>
          <tr>
            <td><em>May 2017</em></td>
            <td><em>Aug 2017</em></td>
            <td>Software Development Researcher</td>
            <td>Monmouth University School of Science</td>
          </tr>
        </tbody>
      </table>
      <hr />

      <h3>Skills</h3>
      <table border="3px" cellspacing="3px">
        <tr>
          <td>
            <table>
              <tr>
                <td>Java</td>
                <td>✯✯✯✯</td>
              </tr>
              <tr>
                <td>Python</td>
                <td>✯✯✯✯</td>
              </tr>
              <tr>
                <td>C++</td>
                <td>✯✯✯✯</td>
              </tr>
            </table>
          </td>
          <td>
            <table>
              <tr>
                <td>iOS Development</td>
                <td>✯✯✯</td>
              </tr>
              <tr>
                <td>Swift</td>
                <td>✯✯✯</td>
              </tr>
              <tr>
                <td>Web Development</td>
                <td>✯✯</td>
              </tr>
            </table>
          </td>
        </tr>
      </table>
      <hr />
      <a href="hobbies.html">My Hobbies</a>
      <a href="contact.html">Contact Me</a>
      <hr />
      <a href="inputs.html">HTML Inputs live demo</a>

    </body>
  </html>

- This part of the module is focused on debugging code provided to us by App Brewery
-     DEBUG PROBLEM 1
- Issue Found: when linking the external css file, the "href" used began with a "/". This means that the root files of a non-hosted are being targeted. This will result in a null target and the browser will use the default css styling. (ERR_FILE_NOT_FOUND)
-     DEBUG PROBLEM 2
- Issue Found: Although everything was correct syntax wise, there was a style attribute used as injected CSS code. (<body style="background-color: white;">)

