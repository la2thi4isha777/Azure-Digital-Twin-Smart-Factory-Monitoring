# Azure Digital Twin - Smart Factory Simulation

factory_equipment = {
    "Robotic Arm A1": {"temperature": 42, "status": "Running"},
    "Cooling System C3": {"temperature": 28, "status": "Active"},
    "Conveyor Belt B2": {"temperature": 39, "status": "Idle"},
    "Hydraulic Press H5": {"temperature": 46, "status": "Running"}
}

def monitor_factory(equipment_data):
    print("🏭 Azure Digital Twin - Smart Factory Monitoring\n")
    for name, data in equipment_data.items():
        temp = data["temperature"]
        status = data["status"]
        alert = "🔥 Overheat Alert!" if temp > 40 else "✅ Temp Normal"
        print(f"{name}: Temp = {temp}°C | Status = {status} | {alert}")

monitor_factory(factory_equipment)
