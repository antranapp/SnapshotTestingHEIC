# SnapshotTestingHEIC 🗜
An extension to SnapshotTesting which allows you to create HEIC images.
The benefit of using HEIC instead of PNG is that it can store as much as image quality as PNG, but with a smaller file size.
You can verify this by looking at SnapshotTestingHEICTests.

## Usage

Once [installed](#installation), _no additional configuration is required_. You can import the `SnapshotTestingHEIC` module, call `SnapshotTesting` following their usage guide and simply provide our `imageHEIC` strategy as below.

```swift
import XCTest
import SnapshotTesting
import SnapshotTestingHEIC

class MyViewControllerTests: XCTestCase {
  func testMyViewController() {
    let vc = MyViewController()
    assertSnapshot(matching: vc, as: .imageHEIC)
  }
}
```

## Installation

### Xcode 11

> ⚠️ Warning: By default, Xcode will try to add the SnapshotTestingStitch package to your project's main application/framework target. Please ensure that SnapshotTestingStitch is added to a _test_ target instead, as documented in the last step, below.
 1. From the **File** menu, navigate through **Swift Packages** and select **Add Package Dependency…**.
 2. Enter package repository URL: `https://github.com/Sherlouk/swift-snapshot-testing-stitch`
 3. Confirm the version and let Xcode resolve the package
 4. On the final dialog, update SnapshotTestingStitch's **Add to Target** column to a test target that will contain snapshot tests (if you have more than one test target, you can later add SnapshotTestingStitch to them by manually linking the library in its build phase)

### Swift Package Manager

### Other

We do not currently support distribution through CocoaPods or Carthage.

## License

This library is released under the MIT license. See [LICENSE](LICENSE) for details.