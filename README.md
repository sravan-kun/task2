def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

def celsius_to_kelvin(celsius):
    return celsius + 273.15

def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

def fahrenheit_to_kelvin(fahrenheit):
    return (fahrenheit + 459.67) * 5/9

def kelvin_to_celsius(kelvin):
    return kelvin - 273.15

def kelvin_to_fahrenheit(kelvin):
    return (kelvin * 9/5) - 459.67

def temperature_converter():
    print("Welcome to the Temperature Converter!")
    print("Select conversion type:")
    print("1. Celsius to Fahrenheit")
    print("2. Celsius to Kelvin")
    print("3. Fahrenheit to Celsius")
    print("4. Fahrenheit to Kelvin")
    print("5. Kelvin to Celsius")
    print("6. Kelvin to Fahrenheit")
    
    while True:
        choice = input("Enter choice (1/2/3/4/5/6): ")
        
        if choice in ['1', '2', '3', '4', '5', '6']:
            temp = float(input("Enter the temperature to convert: "))
            
            if choice == '1':
                print(f"{temp}°C is equal to {celsius_to_fahrenheit(temp)}°F")
            elif choice == '2':
                print(f"{temp}°C is equal to {celsius_to_kelvin(temp)}K")
            elif choice == '3':
                print(f"{temp}°F is equal to {fahrenheit_to_celsius(temp)}°C")
            elif choice == '4':
                print(f"{temp}°F is equal to {fahrenheit_to_kelvin(temp)}K")
            elif choice == '5':
                print(f"{temp}K is equal to {kelvin_to_celsius(temp)}°C")
            elif choice == '6':
                print(f"{temp}K is equal to {kelvin_to_fahrenheit(temp)}°F")
        else:
            print("Invalid input. Please choose a valid option.")
        
        next_conversion = input("Do you want to perform another conversion? (yes/no): ")
        if next_conversion.lower() != 'yes':
            break

    print("Thank you for using the Temperature Converter!")

if __name__ == "__main__":
    temperature_converter()
