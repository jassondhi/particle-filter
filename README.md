

<!-- INTRODUCTION -->
<br />

![Particle Filter - Mars Glider Project](/assets/title.jpg?raw=true "Index")

  <p align="center">
    An implementation of a Particle Filter to localize a robotic glider given only a distance to ground measurement and an altitude estimate. 
  </p>
</p>

<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Estimation](#estimation)
  * [Navigation](#navigation)
* [Powered by Python](#built-with)
* [License](#license)
* [Contact](#contact)

<!-- ABOUT THE PROJECT -->
## About The Project

This is a really cool implementation of a Particle Filter to localize a robotic glider without access to GPS satellites I worked on while taking Artificial Intelligence for Robotics at Georgia Tech.

Our craft has a map of the area it's being dropped into and is dropped within a 250 meter radius of the origin. Our job is to figure out exactly where we are and pilot back to the origin exactly to land.

Due to proprietary code restrictions, I cannot publicly share the code other than a short overview!

### Estimation

![Estimation of the Craft's Current Position](/assets/estimation.gif?raw=true "Estimation of the Craft's Current Position")

Here's an example of how we use the particle filter to estimate the next craft position with the information we have from the radar distance to the ground and the atmospheric height. We have some idea of the topographical makeup of the map and can take a guess at where we are based on the best particles.

The orange highlights the topographic regions of the map. The purple dot is our estimate of where the craft is. The red triangle is the actual position of the craft. You can see the purple dot slowly approach to the actual position of the craft as the particles all begin to converge to the real position.

In this step, we haven't yet navigated anywhere, we have only found the "real" position of the craft. In the next step, we will use this knowledge to pilot back to the origin.


### Navigation

![Craft Navigation Back to Origin](/assets/navigation.gif?raw=true "Craft Navigation Back to Origin")

Here's how we use the estimate of our position to navigate back to the origin. We determine which quadrant we're in and how far we are from the origin and take a greedy approach to get back home full steam ahead!


## Built With
This project was built in Python version 3.8.3 using NumPy.
* [NumPy](https://numpy.org/)

<!-- LICENSE -->
## License
Not distributed for public use.


<!-- Acknowledgements -->
## Acknowledgements
[Title image](https://www.iconfinder.com/icons/2927569/armageddon_asteroid_astronomy_comet_galaxy_meteor_meteorite_icon) is licensed under CC by 3.0.

<!-- CONTACT -->
## Contact
Jasmine Sondhi - [LinkedIn](https://www.linkedin.com/in/jasmine-sondhi/) - jsondhi@outlook.com
