package studeninfosystem;

import java.util.*;
import java.io.*;

public class StudentInfoSystem {

    public static int connector = 0;
    public static int error_checker = 0;

    public static void displayWelcome() {
        for (int i = 1; i <= 3; i++) {
            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
                System.out.println(e);
            }
            System.out.println("******************************************");
        }

        System.out.println("********    JIMMA UNIVERSITY    **********");
        System.out.println("*****    STUDENT INFORMATION SYSTEM  *****");
        for (int i = 1; i <= 3; i++) {
            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
                System.out.println(e);
            }
            System.out.println("******************************************");
        }
        System.out.println("");
    }

    public static void operations(Scanner input) {
        int uinput;
        try {
            do {
                userInput();
                int inserted = input.nextInt();
                input.nextLine();
                uinput = inserted;
                if (uinput >= 0 && uinput <= 3) {
                    selectStudent(inserted);

                    inserted = input.nextInt();
                    input.nextLine();
                    chooseAction(inserted, input);

                    inserted = input.nextInt();
                    input.nextLine();
                    createArray(inserted, input);
                } else {
                    System.out.println("YOUR INPUT IS OUT OF RANGE");
                    System.out.println("Please Try again and choose from the given alterantives");
                }

            } while (uinput != 0);
        } catch (Exception e) {
            System.out.println(e);
            error_checker++;
        }
        if (error_checker > 0) {
            debbugger();
        }
    }

    public static void debbugger() {
        Scanner sc = new Scanner(System.in);
        operations(sc);
        error_checker = 0;
    }

    public static void userInput() {

        System.out.println("\tChoose Your Operation");
        System.out.println("1. To Add a student");
        System.out.println("2. To Show students added before, if any");
        System.out.println("3. To Delete a student");
        System.out.println("0. To EXIT");
        System.out.print("Your Input: ");
        connector = 0;

    }

    public static void selectStudent(int number) {
        connector += number;
        switch (number) {
            case 1:
                System.out.println("Choose The Type of Student You Want To Add: ");
                System.out.println("1. UnderGraduate");
                System.out.println("2. PostGraduate");
                System.out.print("Your Input: ");
                break;
            case 2:
                System.out.println("Choose The Type of Student You Want To Check: ");
                System.out.println("1. UnderGraduate");
                System.out.println("2. PostGraduate");
                System.out.println("3. All");
                System.out.print("Your Input: ");
                break;
            case 3:
                System.out.println("Choose The Type of Student You Want To Delete: ");
                System.out.println("1. UnderGraduate");
                System.out.println("2. PostGraduate");
                System.out.println("3. All");
                System.out.print("Your Input: ");
                break;
            case 0:
                System.out.println("THANK YOU FOR VISITING");
                System.exit(0);
                break;

        }

    }

    public static void chooseAction(int number, Scanner input) {
        if (connector == 1) {
            switch (number) {
                case 1:
                    System.out.println("How Many UnderGraduate Students You Want To Add To The System?");
                    connector += 5;
                    break;
                case 2:
                    System.out.println("How Many PostGraduate Students You Want To Add To The System?");
                    connector += 10;
                    break;
                default:
                    System.out.println("Invalid input, Please Try Again....");
                    break;

            }
        } else if (connector == 2) {
            switch (number) {
                case 1:
                    System.out.println("Choose The Type of Undergraduate Student : ");
                    System.out.println("1. Regular");
                    System.out.println("2. Extension");

                    int chstd = input.nextInt();
                    input.nextLine();
                    if (chstd == 1) {
                        System.out.println("UnderGraduate Regular Students That We have in The System: ");
                        printUnderGraduateRegualrStudent();
                    } else if (chstd == 2) {

                        System.out.println("UnderGraduate Extension Students That We have in The System: ");
                        printUnderGraduateExtensionStudent();
                    } else {

                        System.out.println("your input is invalid");

                    }

                    operations(input);
                    break;

                case 2:
                    System.out.println("PostGraduate Students That We have in The System: ");
                    printPostGraduateStudent();
                    operations(input);
                    break;

                case 3:
                    System.out.println("All of the Students That We have in The System: ");
                    printPostGraduateStudent();
                    printUnderGraduateRegualrStudent();
                    printUnderGraduateExtensionStudent();
                    operations(input);
                    break;

                default:
                    System.out.println("Invalid input, Please Try Again....");
                    operations(input);
                    break;

            }
        } else if (connector == 3) {
            switch (number) {
                case 1:
                    System.out.println("Choose The Type of Undergraduate Student : ");
                    System.out.println("1. Regular");
                    System.out.println("2. Extension");

                    int chstd = input.nextInt();
                    input.nextLine();
                    if (chstd == 1) {
                        deleteUnderGraduateRegular();
                        System.out.println("you have deleted all UnderGraduate Regular students");
                        System.out.println("---------------------------------------------------------");
                    } else if (chstd == 2) {
                        deleteUnderGraduateExtension();
                        System.out.println("you have deleted all UnderGraduate Extension students");
                        System.out.println("---------------------------------------------------------");
                    } else {

                        System.out.println("your input is invalid");

                    }

                    operations(input);
                    break;

                case 2:
                    deletePostGraduate();
                    System.out.println("you have deleted all post graduate students");
                    System.out.println("---------------------------------------------------------");
                    operations(input);
                    break;

                case 3:
                    deletePostGraduate();
                    deleteUnderGraduateRegular();
                    deleteUnderGraduateExtension();
                    System.out.println("you have deleted all students you have in the system");
                    System.out.println("---------------------------------------------------------");

                    operations(input);
                    break;

                default:
                    System.out.println("Invalid input, Please Try Again....");
                    operations(input);
                    break;

            }
        }
    }

    public static void createObject(Regular[] user, int index) {
        for (int i = 0; i < index; i++) {
            user[i] = new Regular();
        }
    }

    public static void createObject(Extension[] user, int index) {
        for (int i = 0; i < index; i++) {
            user[i] = new Extension();
        }

    }

    public static void createObject(PostGraduate[] stud, int index) {
        for (int i = 0; i < index; i++) {
            stud[i] = new PostGraduate();
        }
    }

    public static void createArray(int number, Scanner input) {
        if (connector == 6) {
            System.out.println("Choose The Student Type: ");
            System.out.println("1. Regular");
            System.out.println("2. Extension");

            int chstd = input.nextInt();
            input.nextLine();
            if (chstd == 1) {
                Regular reg[] = new Regular[number];
                createObject(reg, number);
                takeInput(reg, number, input);
            } else if (chstd == 2) {
                Extension ext[] = new Extension[number];
                createObject(ext, number);
                takeInput(ext, number, input);
            } else {
                System.out.println("your input is invalid");

            }

// ther must be some method that ask the user what type of  undergraduate student he wants to add to the system  and we have to create an object of them 
        } else if (connector == 11) {
            PostGraduate[] stud = new PostGraduate[number];
            createObject(stud, number);
            takeInput(stud, number, input);
        }

    }

    public static void takeInput(PostGraduate[] user, int index, Scanner input) {

        System.out.println("insert the student in the below format");
        for (int i = 0; i < index; i++) {
            System.out.print("Id number : ");
            int id = input.nextInt();
            input.nextLine();

            System.out.print("Name : ");
            String name = input.nextLine();

            System.out.print("Gender : ");
            String gender = input.nextLine();

            System.out.print("Age : ");
            int age = input.nextInt();
            input.nextLine();

            System.out.print("Phone No.: ");
            String phone = input.nextLine();

            System.out.print("Address : ");
            String address = input.nextLine();

            System.out.print("Marital Status: ");
            String marital = input.nextLine();

            System.out.print("Previous GPA : ");
            double gpa = input.nextDouble();
            input.nextLine();

            System.out.print(" Current Job : ");
            String job = input.nextLine();

            System.out.print("Previous university: ");
            String pCampus = input.nextLine();

            System.out.print("Educational Background : ");
            String eduBack = input.nextLine();

            user[i].setInfo(id, name, gender, age, phone, address, marital, gpa, job, pCampus, eduBack);
            if (i < index - 1) {
                System.out.println("insert the next Student ********************************\\");
            }
        }
    }

    /*
    In This Method We Will take information of Regular Students from user and pass it to setter
     */
    public static void takeInput(Regular[] user, int index, Scanner input) {

        System.out.println("insert the Student in the below format");
        for (int i = 0; i < index; i++) {
            System.out.print("Id number : ");
            int id = input.nextInt();
            input.nextLine();

            System.out.print("Name : ");
            String name = input.nextLine();

            System.out.print("Gender : ");
            String gender = input.nextLine();

            System.out.print("Age : ");
            int age = input.nextInt();
            input.nextLine();

            System.out.print("Academic Year : ");
            int year = input.nextInt();
            input.nextLine();

            System.out.print("Semister : ");
            int semister = input.nextInt();
            input.nextLine();

            System.out.print("Dorm No.: ");
            int dorm = input.nextInt();
            input.nextLine();

            System.out.print("Assigned Cafeteria: ");
            String cafe = input.nextLine();

            System.out.print("Phone No. : ");
            String phone = input.nextLine();

            System.out.print("Address : ");
            String address = input.nextLine();

            System.out.print("Marital Status of Student: ");
            String marital = input.nextLine();

            user[i].setInfo(id, name, gender, age, phone, address, marital, year, semister, dorm, name);
            if (i < index - 1) {
                System.out.println("Insert the next Student********************************\\");
            }
        }
    }

    public static void takeInput(Extension[] user, int index, Scanner input) {
        System.out.println("insert the Student in the below format");
        for (int i = 0; i < index; i++) {
            System.out.print("Id number : ");
            int id = input.nextInt();
            input.nextLine();

            System.out.print("Name : ");
            String name = input.nextLine();

            System.out.print("Gender : ");
            String gender = input.nextLine();

            System.out.print("Age : ");
            int age = input.nextInt();
            input.nextLine();

            System.out.print("Academic Year : ");
            int year = input.nextInt();
            input.nextLine();

            System.out.print("Extension Type : ");
            String type = input.nextLine();

            System.out.print("Term : ");
            int term = input.nextInt();
            input.nextLine();

            System.out.print("Phone No. : ");
            String phone = input.nextLine();

            System.out.print("Address : ");
            String address = input.nextLine();

            System.out.print("Marital Status : ");
            String marital = input.nextLine();

            user[i].setInfo(id, name, gender, age, phone, address, marital, year, type, term);
            if (i < index - 1) {
                System.out.println("insert the next Student********************************\\");
            }
        }
    }

    public static void printUnderGraduateRegualrStudent() {
        try {
            File myObj = new File("UnderGraduateRegular.txt");
            Scanner myReader = new Scanner(myObj);
            while (myReader.hasNextLine()) {
                String data = myReader.nextLine();
                System.out.println(data);
            }
            myReader.close();
        } catch (FileNotFoundException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }

    public static void printUnderGraduateExtensionStudent() {
        try {
            File myObj = new File("UnderGraduateExtension.txt");
            Scanner myReader = new Scanner(myObj);
            while (myReader.hasNextLine()) {
                String data = myReader.nextLine();
                System.out.println(data);
            }
            myReader.close();
        } catch (FileNotFoundException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }

    public static void printPostGraduateStudent() {
        try {
            File myObj = new File("PostGraduate.txt");
            Scanner myReader = new Scanner(myObj);
            while (myReader.hasNextLine()) {
                String data = myReader.nextLine();
                System.out.println(data);
            }
            myReader.close();
        } catch (FileNotFoundException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }

    public static void deletePostGraduate() {
        try {
            FileWriter myWriter = new FileWriter("PostGraduate.txt");
            myWriter.write("************** PostGraduate Students Information **************\n");
            myWriter.close();
        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }

    public static void deleteUnderGraduateRegular() {
        try {
            FileWriter myWriter = new FileWriter("UnderGraduateRegular.txt");
            myWriter.write("************** UnderGraduate Regular Students Information **************\n");
            myWriter.close();
        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }

    public static void deleteUnderGraduateExtension() {
        try {
            FileWriter myWriter = new FileWriter("UnderGraduateExtension.txt");
            myWriter.write("************** UnderGraduate Extension Students Information **************\n");
            myWriter.close();
        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }

    static void passwordCheck(Scanner input) {
        String Password = null;
        int len;
        String Newpassword;
        String insertedPassword = null;
        FileWriter myWriter;
        String data;
        try {
            File myObj = new File("Password.txt");
            Scanner myReader = new Scanner(myObj);
            while (myReader.hasNextLine()) {
                data = myReader.nextLine();
                Password = data;
            }
            myReader.close();
        } catch (FileNotFoundException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }

        if (Password == null) {
            System.out.println("You are new to the system, please Set New Password...");
            System.out.println("Insert Your Password: ");
            try {
                do {
                    System.out.println("Your password must contain at least 8 characters");
                    myWriter = new FileWriter("Password.txt");
                    Newpassword = input.nextLine();
                    len = Newpassword.length();
                } while (len < 8);
                myWriter.write(Newpassword);
                myWriter.close();

                System.out.println("You have Successfully set your Password.");
                System.out.println("---------------------------------------------------");
            } catch (IOException e) {
                System.out.println("An error occurred.");
                e.printStackTrace();
            }
        } else {
            int max_try = 0;
            do {
                if (Password != null) {
                    if (max_try == 0) {
                        System.out.println("Please enter your password to continue: ");
                    } else {
                        System.out.println("Your password is incorrect,Please try again....");
                    }
                    insertedPassword = input.nextLine();
                    if (insertedPassword == null ? Password == null : insertedPassword.equals(Password)) {
                        break;
                    }
                    max_try++;
                }
                if (max_try == 3) {
                    System.out.println("You have tried 3 times, Access Denied!");
                    System.exit(0);

                }
            } while (Password != insertedPassword);
        }
    }

    public static void main(String[] args) {
        displayWelcome();
        Scanner input = new Scanner(System.in);
        passwordCheck(input);
        operations(input);
    }

}
