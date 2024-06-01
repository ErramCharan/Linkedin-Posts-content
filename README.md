import time
def timer(func):
  def wrapper(*args):
    start=time.time()
    func(*args)
    print('time taken to perform the square function is',func.__name__,time.time()-start,'secs')
  return wrapper 

@timer
def square(num):
  print('print square of',num,'is',num**2)

square(16)


print square of 16 is 256
time taken to perform the square function is square 0.00013256072998046875 secs
