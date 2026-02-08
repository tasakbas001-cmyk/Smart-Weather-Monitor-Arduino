## 🌐 Simulation Note
[▶ Run Simulation in Tinkercad](https://www.tinkercad.com/things/1We2Xs3R0sQ-zhanibek-abilkhamit?sharecode=undefined)

**Please note the differences between the simulation and the physical prototype:**
1. **Sensor:** The simulation uses the **TMP36** sensor because the DHT11 library is not natively supported in this Tinkercad environment. However, the logic remains the same.
2. **Circuit:** The simulation includes a **potentiometer** for LCD contrast. In my physical build, I optimized the design by hardwiring the **V0 pin to GND**, which provides perfect contrast without extra components.
3. **Code:** The code in the tincercard is slightly adjusted for the TMP36 to ensure the simulation runs correctly and it differs from code in repository.
