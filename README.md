## Creating Your First Workflow

### Change the app’s Product Name to a unique name
<img width="1045" alt="スクリーンショット_2023_01_28_17_07" src="https://user-images.githubusercontent.com/47273077/215254797-ee4878e4-dad5-453e-8121-3aa53542c1d4.png">

### Double-click the Debug test host value. Then, change the two references to Coffee to your new product name.
<img width="926" alt="WiFi_と_Clock_と_Item-0" src="https://user-images.githubusercontent.com/47273077/215306251-a540ace6-a025-483c-852e-def13974564b.png">

### Next, open CoffeeViewModelTests.swift and change @testable import Coffee to your new name. Your new import will follow this format:
```swift
import XCTest
@testable import YamamotoCoffee
```
### 
The Report Navigator contains two tabs: Local and Cloud. Local displays all builds your computer runs locally. Cloud contains all builds Xcode Cloud runs in the cloud.
<img width="1032" alt="スクリーンショット_2023_01_28_17_22" src="https://user-images.githubusercontent.com/47273077/215255499-1b471e0a-51c2-4531-b4f4-38d6aee51489.png">


In the Cloud tab, click the Create Workflow button to create your first workflow.
<img width="1094" alt="スクリーンショット_2023_01_28_17_24" src="https://user-images.githubusercontent.com/47273077/215255566-94b3f508-2e11-415c-979b-0579e3c680ef.png">

Xcode Cloud works with apps and frameworks. Select your product and click Next.
<img width="1133" alt="WiFi_と_Clock_と_Item-0" src="https://user-images.githubusercontent.com/47273077/215255676-7a7215f9-456e-4ff5-8ce7-871161a7883f.png">

Xcode allows you to review the workflow before continuing. For now, leave all the settings as the defaults and click Next. Xcode Cloud contacts GitHub to check permissions.
<img width="997" alt="スクリーンショット_2023_01_28_17_28" src="https://user-images.githubusercontent.com/47273077/215255727-b6c23bd6-6421-41c6-af18-bb0b21c4944e.png">

Back in Xcode, the grant access button is no longer available, and you’ll see another green check mark.
<img width="767" alt="スクリーンショット 2023-01-28 17 33 57" src="https://user-images.githubusercontent.com/47273077/215255940-c67bd042-13fe-4549-b956-f1f4f2812ad1.png">

Xcode Cloud requires an app on App Store Connect with your app’s bundle identifier. Lucky for you, Xcode can create the app without even opening a browseXcode Cloud requires an app on App Store Connect with your app’s bundle identifier. Lucky for you, Xcode can create the app without even opening a browser. Click Complete to create your app.
<img width="908" alt="スクリーンショット_2023_01_28_17_35" src="https://user-images.githubusercontent.com/47273077/215256077-9c088a13-6bbb-422b-b14e-b2633f8c6bc6.png">

Go ahead and click Start Build to kick off your very first Xcode Cloud build. Xcode Cloud immediately starts the build and switches to the build info in Xcode. Xcode Cloud also sends you an email when the build finishes.
<img width="757" alt="スクリーンショット_2023_01_28_17_37" src="https://user-images.githubusercontent.com/47273077/215256174-d2a0aa70-3de8-4dcd-9048-59c5819254c4.png">

## Creating a Workflow to Run Tests
In the previous section, you set up a default workflow that built the project. You can now edit it to run tests instead. Right-click Default and select Edit Workflow.

<img width="278" alt="スクリーンショット_2023_01_29_15_38" src="https://user-images.githubusercontent.com/47273077/215309632-912ff9c5-e48e-48d1-bd61-b25fa199ca34.png">


Navigate to General, and change the Name to Test.

<img width="912" alt="スクリーンショット_2023_01_29_15_41" src="https://user-images.githubusercontent.com/47273077/215309763-58394cd0-5147-4045-b7c1-100461a02114.png">

The workflow currently has an archive action in the Actions section. The test workflow only runs tests, so you can delete the archive action. Navigate to Archive – iOS and delete the action using the trash icon in the top right.
<img width="955" alt="スクリーンショット_2023_01_29_15_47" src="https://user-images.githubusercontent.com/47273077/215309964-f83ab86f-595d-4800-a744-f21378f7fe7a.png">

Next, add a test action using the + next to the Actions section title.
<img width="809" alt="スクリーンショット_2023_01_29_15_49" src="https://user-images.githubusercontent.com/47273077/215310069-b30f91b2-6d78-4845-8833-60875da9f6a4.png">

The last section configures which devices the tests run on. Click the + to add iPads to your workflow.
<img width="759" alt="スクリーンショット_2023_01_29_15_52" src="https://user-images.githubusercontent.com/47273077/215310180-624f93fd-fc7f-4023-b867-ccd18bea3186.png">

## Testing the Test Workflow

Manually run the workflow. 
<img width="712" alt="スクリーンショット_2023_01_29_15_55" src="https://user-images.githubusercontent.com/47273077/215310352-1ac7ba95-936f-4caa-a618-b279e43b9ea7.png">

