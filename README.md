# y-extensionkit

This library has been created to make your life easier as a Kotlin Developer.

## Setup
With gradle ;

Step 1. Add the JitPack repository to your build file
Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.yamanf:YExtensionKit:1.0'
	}
---
or with Maven;

Step 1. Add the JitPack repository to your build file

	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
Step 2. Add the dependency

	<dependency>
	    <groupId>com.github.yamanf</groupId>
	    <artifactId>YExtensionKit</artifactId>
	    <version>1.0</version>
	</dependency>

## Usage & examples

There are some examples about how you can use these extensions.

- Print to logcat

        val text = "This is text"
        text.printToLog()

        val user = User(
            name = "Yaman",
            id = 1
        )
        user.printToLog() // With default log tag
        user.printToLog(tag = "USER_INFO") // With custom log tag

- Visibility

        view.gone()
        view.visible()
        view.invisible()

        //  A proper boolean expression should be used for dataFound, loading, and condition.
        view goneIf dataFound
        view visibleIf loading
        view invisibleIf condition

- Easy toast messages

        toast("Toast Message")
        toast(R.string.message)

- Easy snackbar messages

        rootView.snackbar("Snackbar message")
        rootView.snackbar(R.string.message)

- Easily hide keyboard

            hideKeyboard()

- dp and px conversion

        params.setMargins(16.px, 16.px, 16.px, 16.px)

- Digit, Alphabetic, and Alphanumeric Check

        val isValidNumber = "1234".isDigitOnly // Return true
        val isValid = "1234abc".isDigitOnly // Return false
        val isOnlyAlphabetic = "abcABC".isAlphabeticOnly // Return true
        val isOnlyAlphabetic2 = "abcABC123".isAlphabeticOnly // Return false
        val isOnlyAlphanumeric = "abcABC123".isAlphanumericOnly // Return true
        val isOnlyAlphanumeric2 = "abcABC@123.".isAlphanumericOnly // Return 
        
- Date Formatter

        val currentDate = Date().toStringFormat()
        val currentDate2 = Date().toStringFormat(format = "dd-MM-yyyy")
        val date = "2023-01-01".toDate(format = "yyyy-MM-dd")
        

## Contribution

This library is open for contributions, bug reports, and feature requests. Feel free to submit a pull request or create an issue if you find any bugs or have suggestions for new features. Let's make Kotlin development even more enjoyable!
