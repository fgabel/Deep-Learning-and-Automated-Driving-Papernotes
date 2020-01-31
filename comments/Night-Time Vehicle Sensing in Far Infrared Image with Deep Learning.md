# [Night-Time Vehicle Sensing in Far Infrared Image with Deep Learning](https://doi.org/10.1155/2016/3403451)

**Problem**: Autonomous cars are not very good at seeing objects at night - systems dependent on ambient light don't work as well (even though they do to some extent). Also, night traffic and pedestrian/car
behaviours are different and road signs may be visible later, posing a different problem set to designers of autonomous systems
operating at nighttime.

**Solution**: 
* Infrared sensors measure infrared (IR) light radiating objects in their field of 
view (hence *thermal imaging*). This spectrum is independent of ambient light and can be used for nighttime perception.
Below is an example of an image captured by thermal imaging.
 ![BILD](../images/fir_image.png?raw=true "Wireframe001")
 * The authors preprocess an image such as the above by first setting a low threshold to the raw
 pixel values (of 30° Celsius) and then using a connected region search algorithm to segment coherent warm objects.
* Using a Bayes network (not a very spectacular one, check the paper if you're interested),
the authors achieve a "detection rate" of 93% (I assume what they mean is recall, i.e. the number
of cars detected amongst all cars.). This is a bit worse than what state-of-the-art algorithms can do 
at daytime.
 
![BILD](../images/fir_objectdetection_results.png?raw=true "Wireframe001")

**Notes**:
* Compared with the visible spectra camera, the image captured by the FIR spectrum 
camera lacks color and other semantic information. 
* [There are a couple of companies evaluating the use of thermal imaging but the
cost of these sensors is prohibitive.](https://www.futurecar.com/2333/Should-Night-Vision-be-a-Standard-Feature-on-Autonomous-Cars)
* The authors achieve a framerate of 21 FPS which is good enough for automotive applications.
* The resolution of these cameras is typically rather small, making it easy to process the image 
but limiting the usability as a stand-alone sensor.
* All in all, FIR will need to overcome challenges of cost, field of view and increased durability to meet the stringent criteria for automotion-grade sensors. 
