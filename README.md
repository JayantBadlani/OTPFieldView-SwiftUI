# OTPFieldView - SwiftUI 
## One-Time Password Input Field

## Installation
To use OTPFieldView in your SwiftUI project, follow these steps:

Copy the OTPFieldView.swift file into your project.

### And here's an Example of how to use the library with SwiftUI:

```ruby
import SwiftUI

struct ContentView: View {
    @State private var otp: String = ""

    var body: some View {
        VStack {
            OTPFieldView(numberOfFields: 6, otp: $otp)
                .modifier(OTPModifier(pin: $otp))
                .foregroundColor(.blue)
            
            Text("Entered OTP: \(otp)")
        }
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
```
## Features

### Dynamic Field Count: 
You can customize the number of input fields, making it adaptable to various OTP lengths and security requirements.

### Seamless Input: 
OTPFieldView automatically shifts focus between fields, allowing users to enter their OTP smoothly without manual navigation.

### Paste Support: 
Users can paste their OTP code, and OTPFieldView will intelligently input each digit in sequence, enhancing user convenience.

### Numeric Restriction: 
OTPFieldView restricts input to numeric characters only, ensuring accurate OTP entry and preventing input errors.

### Customizable UI: 
You have the flexibility to modify the UI to match your app's design and branding, ensuring a cohesive user experience.

### Compatibility: 
OTPFieldView is compatible with iOS 14.0+ and Swift 5.3+ and can be seamlessly integrated into your SwiftUI project using Xcode 12.0+.

## Contributions Welcome: We welcome contributions and suggestions from the community. If you encounter issues or have ideas for improvements, please feel free to open an issue or create a pull request.

## Inspired by User Needs: This component was inspired by the need for a simple and efficient OTP input field in SwiftUI applications, ensuring that it addresses real-world user requirements.

Feel free to customize and enhance OTPFieldView according to your specific use case, and enjoy its user-friendly features in your SwiftUI app!

## Requirements
iOS 14.0+
Xcode 12.0+
Swift 5.3+

##  Contributions
Contributions and suggestions are welcome! If you find any issues or have ideas for improvements, please open an issue or create a pull request.

## Author
Jayant Badlani

## Acknowledgments
This component was inspired by the need for a simple and efficient OTP input field in SwiftUI applications.
