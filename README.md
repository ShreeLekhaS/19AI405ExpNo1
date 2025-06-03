<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Shree Lekha.S</h3>
<h3>Register Number:212223110052</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

# PROGRAM:
```
import random

rooms = {
    "Room1": 98,
    "Room2": 102,
    "Room3": 97,
    "Room4": 101,
    "Room5": 99
}

performance = 0

def sensor(room):
    return rooms[room]

def actuator(room):
    global performance
    print(f"Treating patient in {room} with temperature {rooms[room]}°F: Prescribed medicine 💊")
    performance += 1

room_list = list(rooms.keys())
random.shuffle(room_list)

print("🏥 AI Agent starts visiting rooms...\n")

for room in room_list:
    performance -= 1
    temp = sensor(room)
    if temp > 100:
        actuator(room)
    else:
        print(f"{room} - No fever ({temp}°F). No treatment needed.")

print("\n✅ Total Performance Score:", performance)

```
# Output:

![image](https://github.com/user-attachments/assets/e7ca6b82-ed0b-46d8-9de7-fde3754bf359)


# RESULT:
The PEAS description for the given AI problem has been succesfully developed using an AI agent
