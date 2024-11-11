# practical
<?php

// Define the Student class
class Student {
    public $roll_no;
    public $name;
    public $branch;
    public $year;

    // Constructor to initialize the attributes
    public function __construct($roll_no, $name, $branch, $year) {
        $this->roll_no = $roll_no;
        $this->name = $name;
        $this->branch = $branch;
        $this->year = $year;
    }

    // Method to display the details of the student
    public function display() {
        echo "Student Details:\n";
        echo "Roll No: " . $this->roll_no . "\n";
        echo "Name: " . $this->name . "\n";
        echo "Branch: " . $this->branch . "\n";
        echo "Year: " . $this->year . "\n";
        echo "-----------------------\n";
    }
}

// Function to take input and create a student instance
function createStudent($studentNumber) {
    echo "Enter details for Student $studentNumber:\n";
    
    echo "Enter Roll No: ";
    $roll_no = trim(fgets(STDIN));

    echo "Enter Name: ";
    $name = trim(fgets(STDIN));

    echo "Enter Branch: ";
    $branch = trim(fgets(STDIN));

    echo "Enter Year: ";
    $year = trim(fgets(STDIN));

    // Create a new Student object
    $student = new Student($roll_no, $name, $branch, $year);

    return $student;
}

// Create three student instances
$student1 = createStudent(1);
$student2 = createStudent(2);
$student3 = createStudent(3);

// Display the details of the students
$student1->display();
$student2->display();
$student3->display();

?>

