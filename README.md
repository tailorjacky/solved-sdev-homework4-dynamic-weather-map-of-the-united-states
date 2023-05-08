Download Link: https://assignmentchef.com/product/solved-sdev-homework4-dynamic-weather-map-of-the-united-states
<br>


 <main class="container" role="main"></main>



5/5 - (1 vote)

<ul class="list-group">

 <li class="list-group-item">In this assignment, you will be making a dynamic weather map of the United States, visualizing temperatures for each state on the map.</li>

 <li class="list-group-item">We will use the <a href="https://darksky.net/dev" target="_blank" rel="noopener">Dark Sky Forecast API </a>from Lab 9 as the data source.</li>

 <li class="list-group-item">Each state will be color-coded per its current temperature as reported by the DarkSky API. There are five gradations of temperature that will be colored as listed in the table in Part 3.4.</li>

 <li class="list-group-item"><b>Download the starter files from <a href="./StudentWebsite.zip">here</a></b></li>

 <li class="list-group-item"></li>

</ul>

All your code goes only inside <b>index.html</b> and <b>index.js</b> in the <b>StudentWebsite</b> folder. Do not modify any other files.

<p class="alignleft h5">API Setup (5 points)

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample3" aria-expanded="false" aria-controls="multiCollapseExample3">Expand</button>

<ul class="list-group">

 <li class="list-group-item">1. Head over to <a href="https://darksky.net/dev" target="_blank" rel="noopener">Dark Sky API</a></li>

 <li class="list-group-item">2. Click Try for free</li>

 <li class="list-group-item">3. Register: fill in your email, password and confirm password</li>

 <li class="list-group-item">4. Head over to your email and click the confirmation link</li>

 <li class="list-group-item">5. You will see the welcome screen after clicking the link. Then in the top right corner click Log in.</li>

 <li class="list-group-item">6. The API that you will need is the One in the “Sample API Call”. It looks something like https://api.darksky.net/forecast/-your-key-here-/37.8267,-122.4233</li>

</ul>

If you’ve already setup an account on darksky(Lab 9), you can use the same account for this assisgnment. Skip this step.

<p class="alignleft h5">Part 1: Reading the SVG (5 points)

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample4" aria-expanded="false" aria-controls="multiCollapseExample4">Expand</button>

<ul class="list-group">

 <li class="list-group-item">We will be working with SVGs for this part. The first step is for you to read up on what SVGs are from the Resources tab above.</li>

 <li class="list-group-item">We need the SVG of the United States Map. This can be found <a href="https://upload.wikimedia.org/wikipedia/commons/1/1a/Blank_US_Map_%28states_only%29.svg" target="_blank" rel="noopener">here</a></li>

 <li class="list-group-item">If you save the SVG locally, it’s not going to work since there’s no way to actually view the XML code for it. So instead head over to the <a href="https://upload.wikimedia.org/wikipedia/commons/1/1a/Blank_US_Map_%28states_only%29.svg" target="_blank" rel="noopener">link</a> provided above, right click and click View Page Source</li>

 <li class="list-group-item"><iframe width="971" height="546" frameborder="0" allowfullscreen data-mce-fragment="1" data-src="https://www.youtube.com/embed/5uxxc8W0Oso" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw=="></iframe></li>

 <li class="list-group-item">Paste the contents you see on the browser in index.html between the ‘Paste World Map Here’ and the ‘End of World Map’ tags <b>POINTS: 5</b></li>

</ul>

<p class="alignleft h5">Part 2: Reading the JS (2 points)

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample5" aria-expanded="false" aria-controls="multiCollapseExample2">Expand</button>

<ul class="list-group">

 <li class="list-group-item">Read the state_info.js into index.html at the ‘Import state_info.js here’ <b>POINTS: 1</b></li>

 <li class="list-group-item">Read the index.js into index.html at the ‘Import index.js here’ <b>POINTS: 1</b></li>

</ul>

<p class="alignleft h5">Part 3: Index.js (88 points)

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample6" aria-expanded="false" aria-controls="multiCollapseExample6">Expand</button>

<ul class="list-group">

 <li class="list-group-item">Paste your API key in index.js where it is marked “Enter your API Key here” <b>4 Points</b></li>

 <li class="list-group-item">If you look at the SVG that you pasted, it has a bunch of IDs that are State Codes. You can change the color of a state code by doing “$(‘#CO’).css(‘fill’, “blue”)” for example.</li>

 <li class="list-group-item">Iterate over each of the rows in the json and make an API call to the Dark Sky API using the latitude and longitude that we saw before. <b>30 Points</b><a href="https://stackoverflow.com/questions/14810506/map-function-for-objects-instead-of-arrays" target="_blank" rel="noopener">Here</a> is how you iterate over a json with a list of Jsons.</li>

 <li class="list-group-item">For each of these, make an API call to DarkSky. <b>24 Points</b>Note that the API calls are limited to 1000 per day, so use them wisely. If you want to learn more about the api response see <a href="https://darksky.net/dev/docs#response-format" target="_blank" rel="noopener">this</a>.If you want to look at the JSON response, see the ‘example_api_response.json’ file in the example folder.If you run out of requests, you may make a new account or try it a day after.</li>

 <li class="list-group-item">The color to be used for a state should be determined based on the following temperature range table. <b>30 Points</b>

  <table class="table">

   <tbody>

    <tr>

     <th>Temperature</th>

     <th>Color</th>

    </tr>

    <tr>

     <td>[default]</td>

     <td>#808080</td>

    </tr>

    <tr>

     <td>Less than equal to 10F</td>

     <td>#6495ED</td>

    </tr>

    <tr>

     <td>Between 11F and 20F</td>

     <td>#7FFFD4</td>

    </tr>

    <tr>

     <td>Between 21F and 30F</td>

     <td>#0000FF</td>

    </tr>

    <tr>

     <td>Between 31F and 40F</td>

     <td>#008B8B</td>

    </tr>

    <tr>

     <td>Between 41F and 50F</td>

     <td>#00BFFF</td>

    </tr>

    <tr>

     <td>Between 51F and 60F</td>

     <td>#F08080</td>

    </tr>

    <tr>

     <td>Between 61F and 70F</td>

     <td>#CD5C5C</td>

    </tr>

    <tr>

     <td>Between 71F and equal to 80F</td>

     <td>#8B0000</td>

    </tr>

    <tr>

     <td>Between 81F and equal to 90F</td>

     <td>#B22222</td>

    </tr>

    <tr>

     <td>Greater than 90F</td>

     <td>#FF0000</td>

    </tr>

   </tbody>

  </table></li>

 <li class="list-group-item"><img decoding="async" alt="sample output" data-src="./sample_output.png" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

  <noscript>

   <img decoding="async" src="./sample_output.png" alt="sample output">

  </noscript></li>

</ul>

The above is a sample of how the final image needs to be

<p class="alignleft h5">Bonus Questions (20 points)

<button class="btn btn-primary btn-sm alignbtn" type="button" data-toggle="collapse" data-target="#multiCollapseExample7" aria-expanded="false" aria-controls="multiCollapseExample7">Expand</button>

<b>Question 1: 10 points</b>



<ol>

 <li>You will create a tooltip to display other information about the weather in each state.</li>

 <li>The tooltip should appear when hovering over any state, and it should update when scrolling across different states. The tooltip should work for all states on the map.</li>

 <li>You can include as many information you want in the tooltip, but some suggested data might be things such as precipitation, humidity, or cloud cover.</li>

</ol>

Note: You’re free to modify the svg element as per your need. You can use any css library to implement tooltip, you can also build your own css tooltip. You can create as many helper functions you want.

<b>Question 2: 10 points</b>

<ul>

 <li>Add wind direction to the tooltip. You can use any css style arrows to show the wind direction.</li>

</ul>

A simple tooltip here.. <iframe width="971" height="546" frameborder="0" allowfullscreen data-mce-fragment="1" data-src="https://www.youtube.com/embed/MNnfe1gx274" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw=="></iframe>

<p class="alignleft h5">