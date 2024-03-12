# HospitalEmployeeTest.java
// Define the abstract class for Hospital Employees
abstract class HospitalEmployee {
    private String empNumber;

    // Constructor
    public HospitalEmployee(String empNumber) {
        this.empNumber = empNumber;
    }

    // Abstract method for providing services
    public abstract void provideService();

    // Get employee number
    public String getEmpNumber() {
        return empNumber;
    }
}

// Doctor class
class Doctor extends HospitalEmployee {
    private String specialization;

    // Constructor
    public Doctor(String empNumber, String specialization) {
        super(empNumber);
        this.specialization = specialization;
    }

    // Provide service method
    public void provideService() {
        System.out.println("Doctor " + getEmpNumber() + " specializes in " + specialization);
    }
}

// Nurse class
class Nurse extends HospitalEmployee {
    // Constructor
    public Nurse(String empNumber) {
        super(empNumber);
    }

    // Provide service method
    public void provideService() {
        System.out.println("Nurse " + getEmpNumber() + " has patients");
    }
}

// Cleaner class
class Cleaner extends HospitalEmployee {
    // Constructor
    public Cleaner(String empNumber) {
        super(empNumber);
    }

    // Provide service method
    public void provideService() {
        System.out.println("Cleaner " + getEmpNumber() + " is sweeping");
    }
}

// Receptionist class
class Receptionist extends HospitalEmployee {
    // Constructor
    public Receptionist(String empNumber) {
        super(empNumber);
    }

    // Provide service method
    public void provideService() {
        System.out.println("Receptionist " + getEmpNumber() + " is attending to patients");
    }
}

// Driver class to test the classes
public class HospitalEmployeeTest {
    public static void main(String[] args) {
        Doctor doctor = new Doctor("D001", "Cardiology");
        Nurse nurse = new Nurse("N001");
        Cleaner cleaner = new Cleaner("C001");
        Receptionist receptionist = new Receptionist("R001");

        // Test the services provided by each employee
        doctor.provideService();
        nurse.provideService();
        cleaner.provideService();
        receptionist.provideService();
    }
}
