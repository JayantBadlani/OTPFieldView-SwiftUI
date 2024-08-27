# OTPFieldView - SwiftUI 
(One-Time Password Input Field) 

<img width="435" alt="Screenshot 2023-10-06 at 6 37 18 PM" src="https://github.com/JayantBadlani/OTPFieldView-SwiftUI/assets/37996543/81cafe17-fdf2-46a5-9401-6abb2dbc21ca">

## Installation
To use OTPFieldView in your SwiftUI project, Copy the **OTPFieldView.swift** file into your project and here's an Example of how to use this with SwiftUI:

```ruby
import SwiftUI

struct ContentView: View {
    @State private var otp: String = ""
    @FocusState private var isOTPFieldFocused: Bool
    private let numberOfFieldsInOTP = 6
    
    var body: some View {
        
        VStack(alignment: .leading, spacing: 8) {
            Text("VERIFICATION CODE")
                .foregroundColor(Color.gray)
                .font(.system(size: 12))
            
            OTPFieldView(numberOfFields: numberOfFieldsInOTP, otp: $otp)
                .onChange(of: otp) { newOtp in
                    if newOtp.count == numberOfFieldsInOTP {
                        // Verify OTP
                    }
                }
                .focused($isTextFieldFocused)
            
            Text("Entered OTP: \(otp)")
        }
        .onAppear {
            DispatchQueue.main.asyncAfter(deadline: .now() + 0.5) {
                isTextFieldFocused = true
            }
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

Feel free to customize and enhance OTPFieldView according to your specific use case, and enjoy its user-friendly features in your SwiftUI app!

## Requirements
iOS 14.0+
Xcode 12.0+
Swift 5.3+

##  Contributions
We welcome contributions and suggestions from the community. If you encounter issues or have ideas for improvements, please feel free to open an issue or create a pull request.

## Author
Jayant Badlani

## Acknowledgments
This component was inspired by the need for a simple and efficient OTP input field in SwiftUI applications, ensuring that it addresses real-world user requirements.
