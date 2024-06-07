# Vehicle-Diagnostics-and-Monitoring-system-
class Vehicle:
    def __init__(self, speed=0, fuel_level=100, engine_temperature=70):
        self.speed = speed
        self.fuel_level = fuel_level
        self.engine_temperature = engine_temperature

    def update_speed(self, speed):
        self.speed = speed
        print(f"Speed updated to {self.speed} km/h")

    def update_fuel_level(self, fuel_level):
        self.fuel_level = fuel_level
        print(f"Fuel level updated to {self.fuel_level}%")

    def update_engine_temperature(self, engine_temperature):
        self.engine_temperature = engine_temperature
        print(f"Engine temperature updated to {self.engine_temperature} °C")

    def get_status(self):
        status = {
            "speed": self.speed,
            "fuel_level": self.fuel_level,
            "engine_temperature": self.engine_temperature
        }
        return status

    def check_issues(self):
        issues = []
        if self.speed > 120:
            issues.append("Speed exceeds the safe limit!")
        if self.fuel_level < 10:
            issues.append("Fuel level is critically low!")
        if self.engine_temperature > 90:
            issues.append("Engine temperature is too high!")
        return issues
