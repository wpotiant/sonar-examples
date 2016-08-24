This example demonstrates how to import Xcode Coverage data (aka ProfData) to SonarQube.

1. Run from "swift-coverage-example"
  * xcodebuild -scheme swift-coverage-example -enableCodeCoverage YES -derivedDataPath . clean build test
  * xcrun llvm-cov show -instr-profile=Build/Intermediates/CodeCoverage/Coverage.profdata Build/Intermediates/CodeCoverage/Products/Debug/swift-coverage-example.app/Contents/MacOS/swift-coverage-example > Coverage.report
  * sonar-scanner
2. Verify that for the project "swift-coverage-example" the coverage value is 50%.
