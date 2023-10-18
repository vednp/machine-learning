
## install Opencv-python

- Windows

  pip install opencv-python

- _install Opencv-python on Linux or Mac_

  pip3 install opencv-python

## Run the code

- windows: :point_down:

  python distance.py

  ------ OR ---------

  python Updated_distance.py

- linux or Mac :point_down:

  python3 distance.py

  ------ OR ---------

  python3 Updated_distance.py

### :bulb:_Focal Length Finder Function Description_ :bulb:

```python
# focal length finder function
def focal_length(measured_distance, real_width, width_in_rf_image):

    focal_length_value = (width_in_rf_image * measured_distance) / real_width
    #return focal length.
    return focal_length_value

```

The Focal Length finder Function Tacks Three Arguments:

`measured_distance` It is distance which we have measured while capturing reference image:straight*ruler:. \*\*\_From object to Camera*\*\* which is `Known_distance = 72.2 #centimeter`

`real_width` Its measure with width of object in real world, here i measure the width of face in real world which was `Known_width =14.3 #centimeter`

`width_in_rf_image` it width of object in the image/frame it will be in **pixels**

### :bulb:_Distance Finder Function Description_ :bulb:

```python
# distance estimation function

def distance_finder(focal_length, real_face_width, face_width_in_frame):

    distance = (real_face_width * focal_length)/face_width_in_frame
    return distance

```

This Funciton Taks Three Argument,

` Focal_Length` it is focal length, out of **FocalLength** finder function.

`real_face_width` Its measure width of object in real world, here i measure the width of face in real world which was `Known_width =14.3 #centimeter`

`face_width_in_frame` width of face in the frame, unit will pixels here.



