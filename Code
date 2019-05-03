import RPi.GPIO as GPIO
import time
ledP =11
ledU =16
ledS =13
buzzer =18
flame =12
gasSensor=22

def setup():
    GPIO.setmode(GPIO.BOARD)
    GPIO.setup(ledP,ledU,ledS,buzzer,flame,gasSensor,GPIO.OUT)
    GPIO.output(ledP,ledU,ledS,buzzer,GPIO.HIGH)
def led():
    while True:
    GPIO.output(ledP,GPIO.LOW)
    time.sleep(3)
    GPIO.output(ledP,GPIO.HIGH)
    time.sleep(3)
def flame():
    while True:
    GPIO.output(flame,GPIO.LOW)
    GPIO.output(ledU,GPIO.LOW)
    GPIO.output(buzzer,GPIO.LOW)
    time.sleep(300)
    GPIO.output(buzzer,GPIO.HIGH)
    time.sleep(5)
    GPIO.output(ledU,GPIO.HIGH)
def gas():
    while True:
    GPIO.output(gasSensor,GPIO.LOW)
    GPIO.output(ledS,GPIO.LOW)
    GPIO.output(buzzer,GPIO.LOW)
    time.sleep(300)
    GPIO.output(buzzer,GPIO.HIGH)
    time.sleep(5)
    GPIO.output(ledS,GPIO.HIGH)
def destory():
    GPIO.output(ledP,GPIO.HIGH)
    GPIO.output(ledP,GPIO.HIGH)
    GPIO.output(buzzer,GPIO.HIGH)
    GPIO.output(ledU,GPIO.HIGH)
    GPIO.output(ledS,GPIO.HIGH)
    GPIO.cleanup()

if _name_=='_main_':
    setup()
    try:
        led()
        flame()
        gas()
    except KeyboardInterrupt:
        destory()




