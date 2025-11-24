print("=== Patient Health Monitoring System ===")
patients = []  
def add_patient():
    print("\n--- Add Patient ---")
    name = input("Enter patient name: ")
    age = input("Enter patient age: ")
    bp = input("Enter blood pressure (ex: 120/80): ")
    sugar = input("Enter sugar level (mg/dL): ")
    temp = input("Enter body temperature (°C): ")
    patient = {
        "name": name,
        "age": age,
        "bp": bp,
        "sugar": int(sugar),
        "temp": float(temp)
    }
    patients.append(patient)
    print("Patient added successfully!\n")
def view_patients():
    print("\n--- Patient Records ---")
    if len(patients) == 0:
        print("No patients found.\n")
        return
    for i, p in enumerate(patients):
        print(f"{i+1}. {p['name']} | Age: {p['age']} | BP: {p['bp']} | Sugar: {p['sugar']} | Temp: {p['temp']}")
    print()
def analyze_health():
    print("\n--- Health Analysis ---")
    if len(patients) == 0:
        print("No patients to analyze.\n")
        return
    for p in patients:
        print(f"\nHealth Report for {p['name']}")
        if p["sugar"] > 140:
            print(" - High sugar detected")
        else:
            print(" - Sugar level normal")
        if p["temp"] > 37.5:
            print(" - Fever detected")
        else:
            print(" - Normal temperature")
        if p["bp"] != "120/80":
            print(" - BP not normal")
        else:
            print(" - BP normal")
    print()
def save_to_file():
    print("\nSaving patient data to file...")
    with open("patients.txt", "w") as f:
        for p in patients:
            f.write(f"{p['name']}, {p['age']}, {p['bp']}, {p['sugar']}, {p['temp']}\n")
    print("Data saved to 'patients.txt'\n")
while True:
    print("1. Add Patient")
    print("2. View Patients")
    print("3. Analyze Health")
    print("4. Save to File")
    print("5. Exit")
    choice = input("Enter your choice: ")
    if choice == "1":
        add_patient()
    elif choice == "2":
        view_patients()
    elif choice == "3":
        analyze_health()
    elif choice == "4":
        save_to_file()
    elif choice == "5":
        print("Exiting program...")
        break
    else:
        print("Invalid choice. Try again.\n")
