# Senior iOS Engineer Coding Challenge RoofStacks
A coding challenge for prospective Senior iOS Developers applying for a role on the RoofStacks iOS developer team.

### Table of Contents

- [Goals](#goals)
- [Preparing Your Local Development Env](#preparing-your-local-development-env)
- [Submission Details and Evaluation Criteria](#submission-details-and-evaluation-criteria)
	- [Assignment](#assignment)
	- [Evaluation and Scoring](#evaluation-and-scoring)
		- [Scoring](#scoring)
- [Dev Team Swift and iOS Documentation Standards](#dev-team-swift-and-ios-documentation-standards)

## Goals

> Keep in mind that **there are no tricks**: each of these expectations are both able to be met, and justifiable development approaches given the assignment.

In order to set transparent expectations, the following list enumerates the *minimum* concepts that we expect to see demonstrated when evaluating your submission.

- Demonstrated mastery of advanced programming concepts in swift for Apple platforms, including
	- MVVM or VIP (Clean Swift) application architecture
		- Most-importantly: fully XCTest-able view controllers & classes (aka independent business logic from the UI / IB interface)
	- Protocol-oriented programming
	- Object-oriented programming
	- Generics
	- UIScene delegation in iOS 13.*
	- Class, object, and attribute privacy and access-control levels
	- The Codable protocol
	- Working with RESTful APIs & raw JSON data
	- URLSession & native networking in Swift
	- Demonstrated experience working with data structures that are relevant to the assignment

- Demonstrated experience with Xcode environments / schemes, & application capabilities, including:
	- Shared schemes
	- Elimination of OS activity debugger logs
	- Sourcing environment variables from the Xcode env when running a target as debug
	- Location services capabilities, including entitlement requirements, plist requirements, & user-permission requests / handling.
	- Enabling XCTest code coverage calculations *for the framework target only*.

- Working knowledge & experience with fully cross-platform, cross-technology framework development techniques, including:
	- Full support for both Cocoapods & Swift Package Manager in a single framework repository
	- Full support for **all** Xcode-supported device classes, *including* macOS (aka macCatalyst).
	- Cocoapod framework development with bundled resources
	- Proper referencing of resource bundles that are not part of the main bundle (located within a framework’s bundle and properly sourced from the framework vs main bundle).
	- 0 third party dependencies for custom frameworks
	- Development of an example application that fully implements the project’s cocoapod framework


- Demonstrate experience with advanced Interface-builder concepts, including:
	- Strategies for proper sourcing & instantiation of interface builder .xib & .storyboard files that belong to an encapsulated framework
	- Variable autolayout traits for universal applications (iOS & iPadOS) that support all device classes & device orientations

- Clean-code practices, including
	- Single responsibility principal (SRP)
	- Avoidance of overly complex code and common pitfalls such as cyclomatic dependencies, repeated code, large function signatures, very long lines of code, etc.
	- Standard, quick-help & apple supported documentation of objects, extensions, object attributes, etc.-- especially if parameters or return types are specified in a function signature or initializer.

- Advanced experience using Xcode’s XCTest Suite, including:
	- 100% code coverage in XCTests for the framework target
	- Writing XCTests with expectations to succeed.
	- Writing XCTests with expectations to fail.
	- Expecation / Wait / fulfill for asynchronus testing processes.
	- Recording & running UITests using the framework’s example application.


> Protip: if you feel as though you are adding something that is listed as a goal, but you do not feel that you have a good or clear justification for where or why you are adding it, you may be adding that feature / functionality in the wrong or non-optimal part of your assignment’s codebase.

## Preparing Your Local Development Env

- Check your local version of Xcode
	- The very **latest release version** of Xcode is required.
		- Beta versions of Xcode should **not** be used.
- Check your local swift version.
	- **Swift version 5.2 (or higher)** (installed with latest Xcode)
- Check your local swift-tools version.
	- **Swift-Tools version 5.2 (or higher)** is required
	- Install from [Swift.org](https://swift.org) if your local tools are not 5.2 or higher (should be by default when installing Xcode)
- The targeted iOS version for any submission should be **iOS 13.0**
	- In general, make sure to double check your project settings.
	- There is a starter project with some of this configured already, but you’ll need to make sure the final matches the requirements.

All of the goals and requirements for your local ENV and general performance of work enumerated here are the *same* as what you will need to perform the work on a day-to-day basis, so consider this challenge as both a test of your skills, and an orientation to our development workflow for senior engineers. (aka, no lost time if you do end up joining the team).

## Submission Details and Evaluation Criteria

### Evaluation and Scoring
During the completion of this challenge, you will be expected to demonstrate experience with several technologies that are key components of our application development workflow, and that you will work with every day on our team.

You will also demonstrate a more general mastery of advanced software development & application development concepts in Swift for Apple platforms.

#### Scoring
**30 Points**: Meeting of the goals enumerated in the “Goals” section below.

- There are exactly 30 child bullets within 5 parent bullets in the Goals section below. They are added up as follows:
	- 1 point if fully met
	- .5 if not fully met but attempted
	- 0 if not met and not attempted.

**50 Points**: Attention to detail & careful following of assignment instructions (including submission). These are graded all-or-nothing.

- **20 pts**: Following Github instructions as specififed, including branch naming conventions, inclusion of all files and folders, properly using draft PRs and proper opening of PR with review request.

- **15 pts**: All assignment criteria including features & technologies are present in submission.
	- Assignment criteria will be enumerated
	- each bullet represents 1 requirement
	- partial points for this category will be awarded by divding 20pts by the number of requirements on the assignment. (ex: 10 requirements == 2pts each)
- **5 pts**: Basic security hygiene is practiced without exception, including:
	- No authentication credentials or API keys are hard-coded in the submission project or framework example project (use env vars for your submission).
	- No hard-coded URLs (use env vars for your submission).
	- No blanket enablement of arbitrary loads (don’t change default NSTransportation Security settings to blanket-allow HTTP requests)
	- Any insecure HTTP domains used are specifically whitelisted / enumerated in info.plist

- **10 pts**: Documentaion
	- **5pts**: All public types, functions, vars, classes, extensions, etc are documented using standard swift documentation and according to our dev team documentation standards.
	- **5pts**: All private types, functions, vars, classes, extensions, etc are documented using standard swift documentation and according to our dev team documentation standards.

**20pts**: On-time submission from the moment of your submission branch is created (see the assignment for the submission time window). This is all-or-nothing, any late submission gets 0pts in this grading category.


**Total:** 100 possible points

## Dev Team Swift and iOS Documentation Standards

We use the standard Swift documentation approach supported in Xcode and used by Apple, however, we do have some sytlistic standards that you should adopt for your submission:

- Do not use Pragma / Mark at all
- Triple slashes > block documentation

**Why not block documentaion?**

- Harder to skim & read than triple slashes because it doesn’t stand out on the left margin of the file
- Harder to format when writing documentation than triple slashes
- It is fully compatible with [Jazzy](https://github.com/realm/jazzy) which we use to auto-generate internal documentation for development team reference.
- Because this is our standard on all existing projects, consistency is a major factor when making standardization decisions
- It perfectly suits our needs now and is the most likely to continue suiting our needs in the future.

**Why not Pragma / Mark?**

- If you never developed with Obj-C (most new / junior devs), it is entirely unclear what Pragma / Mark even means, it’s a very arcane tool at this point in history
- Pragma / Mark will probably not live as long as Swift doc, given the shift to Swift on an industry-level
- We want to avoid having to edit all of our code documentaion if support is ever dropped for it by Apple or [Jazzy](https://github.com/realm/jazzy).


**Standard Formatting Example**
See this Example for the most common Swift doc features we use, the formatting approach, and ordering:

```swift
/// Greets the user by name, as a function.
///
/// - Precondition: The user must have a name
///
/// - Parameters:
///		- name: `String`, representing the name
/// 	of the person the function should greet.
///
/// - Returns: `String`, the greeting interpolated
/// with the value of the `name` argument.
///
/// - Note: Functions are very conversational
/// and friendly if you get to know them.
///
/// - Warning: Don’t mention ternary operators
/// or computed properties to a function, they
/// get very jealous.
///
func aFunc(name: String) -> String {
	return “hello \(name), I am a function.”
}
```

**Additional Info**

Notes:

- The ordering above is the exact ordering you should use in your documentation, in descending order as demonstrated.
- The sections for `Precondition`, `Note`, and `Warning` are not always required or necessary, but definitely use them if they are.

Tips:

- Your documentation changes and updates should reflect in realtime when you access the QuickHelp menu
	- Right click a function signature, class / object definition, or variable
	- Click “QuickHelp” to see your documentation.
