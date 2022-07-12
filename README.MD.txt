wrote a simple python script which captures images every 5 seconds and saves it to a directory 
in order to simulate and always running script, created an indefinite while loop after taking a single image
then check for the status of the script by using the command mentioned in the tutorial 

the script for test: 
"""
import time
import picamera
counter = 0
with picamera.PiCamera() as camera:
    for each in range(5):
        counter +=1
        camera.start_preview()
        time.sleep(5)
        camera.capture("/home/pi/images/image" + str(counter) + ".jpg")
        camera.stop_preview()
        while(1):
            time.sleep(1)


"""
