# Lab 02: Building a web map with HTML, CSS, and Javascript

For this lab assignment, first complete the Lesson 02 and edit the *index.html* file included within the *lesson-02-data/* directory. Retain this completed file as a web map page template within that directory. Create a copy of this *index.html* file within your *lab-02/* directory, and edit this file to meet the following requirements:

1. Within the JavaScript, edit the latitude and longitude coordinates to center the map upon your hometown (or a place you have lived and loved). Adjust the zoom level value if you need to (whole integer numbers only)

	```javascript
	var options = {
		center: [38.0406, -84.5037],
		zoom: 12
	}
	```
2. Modify the h1 page heading with a fun description of your map which includes the name of your town or city
3. Add a new paragraph beneath the h2 heading "About this map". Make the content of this paragraph "Map Authored By ..." and your name.
4. Replace the Lorem Ipsum paragraph text used in Lesson 02 with a paragraph describing some interesting geographical (cultural or physical) aspects of your city.
5. Read the following excerpt from page 80 of John Pickles' (2004) *[A History of Spaces: Cartographic Reason, Mapping and the Geo-Coded World](https://books.google.com/books/about/A_History_of_Spaces.html?id=BGJTas8fnpYC). Write an additional paragraph in response to the passage and how your city is represented on the map.

>THE CARTOGRAPHIC GAZE [...] has come to see itself as a technical-scientific practice of representing (mirroring) nature. It has accepted a universalist logic, underpinned by commitments to particular forms of parametric space, geometry and scale. It is, above all, a controlling gaze rendering the broad swaths of worldly complexity and enormity in miniature form for a discrete purpose. And, as the history of mapping demonstrates, the ordering principles of the cartographic gaze have always had a political intent and/or consequences. The cartographic gaze is dominated by a commitment to modeling a Gods eye view, what Donna Haraway (1991) called the 'God-trick'. This transcendental positioning is both the view from above, an elevated two-point perspective bird's-eye view, *and* an all seeing eye that views everywhere at the same time.

When completed, add and commit these changes to your copy of the *index.html* file in your local repository (within your *lab-02/* directory), and then push this file to your remote GitHub account for submission.
