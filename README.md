# simulations
Various physics sumlations

## 1. Simple harmonic oscillator (простой гармонический осциллятор)

I asked ChatGPT `Easiest in terms of code and most basic physics simulation that includes ordinary differential equations`. It suggested me to simulate simple harmonic oscillator.

Я задал ChatGPT вопрос `Easiest in terms of code and most basic physics simulation that includes ordinary differential equations`. Оно предложило мне просимулировать простой гармонический осциллятор.

<details>
  <summary>ChatGPT output (ответ ChatGPT)</summary>
  
  One example of an easy-to-implement physics simulation that involves ordinary differential equations is a simple harmonic oscillator. This can be modeled using the following equation:
  `m * d^2x/dt^2 + kx = 0`. Where m is the mass of the object, k is the spring constant, x is the displacement from equilibrium, and t is time. This equation can be solved using numerical methods such as Euler's method or Runge-Kutta methods.
  To implement this simulation in code, one could use a simple loop to update the position and velocity of the object at each time step:
  
  ```python3
  # Define initial conditions
  x = 0.5 # Initial position
  v = 0 # Initial velocity
  m = 1 # Mass
  k = 1 # Spring constant
  dt = 0.01 # Time step
  t = 0 # Starting time
  end_time = 10 # End time
  
  # Loop over time steps
  while t < end_time:
    # Calculate acceleration using ODE
    a = -k*x/m
    
    # Update position and velocity using Euler's method
    x += v*dt
    v += a*dt
    
    # Increment time
    t += dt
    
    # Print current position and time
    print("Time:", t, "Position:", x)
  ```
  
  This simulation would produce a graph of the object oscillating back and forth around
  its equilibrium point, with a period determined by the mass and spring constant.
</details>

I questioned myself: what object exactly do we simulate? What is a simple harmonic oscillator? Decided to google it.

Я задался вопросом: какой объект мы на самом деле симулируем? Что такое простой гармонический осциллятор? Решил поискать в интернете.

<details>
  <summary>Result (wikipedia)</summary>
  TODO: paste EN wikipedia here.
</details>

<details>
  <summary>Результат (википедия)</summary>
  Представляет собой вибрирующую систему, характеризующуюся линейной величиной сброса.
  Для механической системы это означает, что существует сила, которая противодействует
  увеличению отклонения с пропорционально возрастающей силой. После внешнего толчка
  гармонический генератор совершает синусоидальные колебания вокруг своего положения
  покоя, причем продолжительность колебаний не зависит от величины отклонения.
  Примерами гармонических генераторов являются пружинные маятники, электрические
  колебательные контуры и камертоны.
</details>
