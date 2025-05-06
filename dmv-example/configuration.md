# Configuration

## **Config File (`config.lua`)**

* **Config.Debug**: Toggles debug mode. Set to `true` to enable detailed logging for troubleshooting.
* **Config.WarningCount**: Number of warnings allowed during practical exams before failing.
* **Config.TheoryExamCurrentPercent**: Percentage of questions that must be answered correctly to pass the theory exam.
* **Config.MoneyRemoved**: Determines where money is deducted from, either 'cash' or 'bank'.
* **Config.Language**: Sets the language for the script. Default is 'en' for English.
* **Config.TheoryExamTime**: Duration of the theory exam in minutes.
* **Config.Blip**: Configures the map blip for the DMV school.
  * `haveBlip`: Shows or hides the blip.
  * `coords`: Location of the blip.
  * `name`: Name displayed on the map.
  * `sprite`, `color`, `scale`, `display`: Visual settings for the blip.
* **Config.NPC**: Defines NPC settings for interaction.
  * `model`: NPC model type.
  * `coords`: NPC location.
  * `heading`: Direction NPC faces.
  * `text`: Text displayed when near the NPC.
  * `eventName`: Event triggered when interacting with the NPC.
  * `target`: If `true`, uses a targeting system; if `false`, uses text UI.
* **Config.CheckPoint**: Settings for checkpoints in practical exams.
  * `color`: Color of the checkpoint.
  * `type`: Type of checkpoint marker.
* **Config.Tests**: Configurations for different vehicle tests.
  * `Vehicle`: Type of vehicle used in the test.
  * `speedLimit`: Maximum speed allowed during the test.
  * `time`: Time limit for the test.
  * `VehicleSpawn`: Spawn location for the vehicle.
  * `Checkpoints`: List of checkpoints with coordinates and radius.
* **Config.DefaultLicense**: Default settings for licenses.
  * `name`, `label`, `description`: Details of the license.
  * `img`: Image associated with the license.
  * `price`, `theoryPrice`: Cost of obtaining the license.
  * `expire`: Expiration period in days.

***

## **Questions Example**

```lua
-- Example for legal_question.lua
{
    question = "What is the speed limit in a residential area?",
    a = "30 km/h",
    b = "50 km/h",
    c = "60 km/h",
    correct = "b",
    img = "path/to/image.png" -- Include if there's an image, otherwise omit - or url
}
```

* **question**: The text of the question.
* **a, b, c**: Answer options.
* **correct**: The correct answer option.
* **img**: Path to an image related to the question (optional).

***

## Locale&#x20;

```lua
Locale = {
    ['en'] = {
    ['title'] = 'DMV\nSCHOOL',
    ['page-2-description'] = 'Your journey to the streets of Los Santos starts here! Get your driver’s license, learn the rules of the road, and master safe driving with our expert instructors. Whether you\'re a beginner or need a refresher, we’ve got you covered. \n Drive smart. Drive safe. Drive legal!',
    ['license'] = 'Licenses',
    ['registered'] = 'Registered:',
    ['expired'] = 'Expired:',
    ['back'] = 'Back',
    ['exit'] = 'Exit',
    ['choose_test'] = 'Choose Test',
    ['driver_license'] = 'Vehicle',
    ['driver_license_description'] = 'Vehicle license for driving on the road with a car , this license is for all vehicles that have a steering wheel and pedals ',
    ['bike_license'] = 'Bike',
    ['bike_license_description'] = 'this license is for riding a bike on the road located in los santos so you can ride a bike in the city ',
    ['plane_license'] = 'Plane',
    ['plane_license_description'] = 'this license is for flying in the air with a plane located in los santos so you can fly in the city ',
    ['boat_license'] = 'Boat',
    ['boat_license_description'] = 'this license is for driving on the water with a boat located in los santos ',
    ['truck_license'] = 'Truck',
    ['truck_license_description'] = 'this license is for driving a truck on the road located in los santos so you can drive a truck in the city or in the country ',
    ['drive_theory'] = 'Drive Theory',
    ['drive_theory_description'] = 'this theory is for driving on the road with a car located in los santos so you can drive a car in the city or in the country ',
    ['bike_theory'] = 'Bike Theory',
    ['bike_theory_description'] = 'this theory is for riding a bike on the road located in los santos so you can ride a bike in the city ',
    ['plane_theory'] = 'Plane Theory',
    ['plane_theory_description'] = 'this theory is for flying in the air with a plane located in los santos so you can fly in the city ',
    ['boat_theory'] = 'Boat Theory',
    ['boat_theory_description'] = 'this theory is for driving on the water with a boat located in los santos so you can drive a boat in the city or in the country ',
    ['truck_theory'] = 'Truck Theory',
    ['truck_theory_description'] = 'this theory is for driving a truck on the road located in los santos so you can drive a truck in the city or in the country ',
    ['theory'] = 'Theory Exam',
    ['theory_description'] = 'in this test you need to answer questions correctly to pass the exam and get your license',
    ['ride'] = 'Practical Test',
    ['ride_description'] = 'in this test you need to drive or fly on the road or in the air to pass the test successfully',
    ['already_have'] = 'You have already passed this test',
    ['already_have_header'] = 'Error',
    ['theory_exam_title'] = 'Theory Exam',
    ['theory_passed'] = 'You passed the theory exam!',
    ['theory_failed'] = 'You failed the theory exam! Try again.',
    ['practical_test_started'] = 'Practical test started. Follow the checkpoints.',
    ['practical_passed'] = 'Congratulations! You passed the practical test.',
    ['practical_failed'] = 'You failed the practical test. Try again.',
    ['need_to_pass_theory'] = 'You need to pass the theory exam first! or you dont have enough money to pay for the practical test in bank account',
    ['need_to_pass_theory_header'] = 'ERROR',
    ['time_finished_theory'] = 'Time is up!',
    ['time_finished_theory_header'] = 'ERROR',
    }
}
```

