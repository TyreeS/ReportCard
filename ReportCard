/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package bequia.sda.primary.school.report.cards;

/**
 *
 * @author tsmith
 */

import java.util.Scanner;

public class BequiaSDAPrimarySchoolReportCards {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
               
        Scanner input = new Scanner(System.in);
        
        
        String first_name = " ", last_name = " ", letter_grade = " ", message = " ", gender = " ";
        int age = 0, class_size, standard;
        double mathematics, grammar, creative_writing, science, social_studies, average_mark = 0/*, Percentage*/;
        
        //This would accept and print the first 15 submissions.
        //However, the length of Array determined by user inputing the number of submissions to be submitted.
        System.out.print("Enter size of class: ");
        class_size = input.nextInt();
        
        //Collecttion of Arrays used to store intformation gathered from the user
        //Array size set to 15
        char [] FName = new char [class_size];
        
        String [] LName = new String [class_size];

        String [] Gender = new String [class_size];
        
        int [] Standard = new int [class_size];
        
        int [] Age = new int [class_size];

        double [] Overall = new double [class_size];

        String [] Grade = new String [class_size];

        String [] Promotion = new String [class_size];
        
        /*for loop used to loop throught the user input questions. 
        The length of the for loop is determined by the user's input of the 
        size of the class  prompted in the beginning.*/
        //for loop set for a size of 15
        for (int i = 0; i < class_size; i++){

            //User input questions used to gather Array data
            System.out.print("Enter first name: ");
            first_name = input.next();
            char initial = first_name.charAt(0); //Initializes the first name to the first character.
                FName[i] = initial; //Stores user input to the respective Array
            
            System.out.print("Enter last name: ");
            last_name = input.next();
                LName[i] = last_name;
                
            System.out.print("Enter gender eg. Male or Female: ");
            gender = input.next();
                Gender[i] = gender;
            
            System.out.print("Enter class to be graduated from ie 1 - 4: ");
            standard = input.nextInt();
                Standard [i] = standard;

            System.out.print("Enter age: ");
            age = input.nextInt();
                Age[i] = age;

            System.out.print("Enter Mathematics Grade: ");
            mathematics = input.nextInt();

            System.out.print("Enter Grammar Grade: ");
            grammar = input.nextInt();

            System.out.print("Enter Social Studies Grade: ");
            social_studies = input.nextInt();

            System.out.print("Enter Science Grade: ");
            science = input.nextInt();

            System.out.print("Enter Creative Writing Grade: ");
            creative_writing = input.nextInt();

            System.out.println(); //Skipped line for spacing 
            
            //Methods used to determine percentage grade and promotion.
            average_mark = Percentage(mathematics, grammar, social_studies, science, creative_writing);
                Overall[i] = average_mark;

            letter_grade = Grade(average_mark);
                Grade[i] = letter_grade;
            
            message = Promotion(age, average_mark);
                Promotion[i] = message;  
                        
                             
            }
            //Print statments or results
            System.out.println("\t\t\tBequia S.D.A Primary School 2019 Student Records");
            System.out.println("\tNAME   \t\tAGE\tGENDER\t  OVERALL\tGRADE\t   PROMOTION MESSAGE\t\tGRADUATING CLASS");
            
            //for loop controls the number of print statements created.
            //loop set to size of 15 to print the first 15 submissions.
            for (int i = 0; i < class_size; i++){
                //Printf output
                //System.out.printf("\t%s. %s\t%d\t%s\t  %.1f\t\t%s\t   %s\tStandard %d\n", FName[i], LName[i], Age[i], Gender[i], Overall[i], Grade[i], Promotion[i], Standard[i]);
                //Print output
                System.out.println("\t" + FName[i] + ". " + LName[i] + "\t" + Age[i] + "\t" + Gender[i] + "\t  " + Overall[i] + "\t\t" + Grade[i] + "\t" + "   " + Promotion[i] + "\t" + "Standard " + Standard[i]);
                System.out.println(); //Skipped line for spacing 
            }
            
            
    }
    //Percentage method used to calculate overall percentage of each student. double was usaed to get exact value
    //Values derived from user input.
    public static Double Percentage (double mathematics, double grammar, double social_studies, double science, double creative_writing){
       
        double average_mark; 
        
            average_mark = (mathematics + grammar + social_studies + science + creative_writing) / 5;
            return average_mark;
    }
    /*Grade method used to calculate letter grade based on overall percentage.
    if statements were used for range values.*/
    public static String Grade (double average_mark){
        
        String letter_grade = " ";
        
            if (average_mark > 89 && average_mark <= 100){
                letter_grade = "A+";
            }
            
                else if (average_mark > 84){
                    letter_grade = "A";
                }
            
                    else if (average_mark > 79){
                        letter_grade = "A-";
                    }
            
                        else if (average_mark > 76){
                            letter_grade = "B+";
                        }
            
                            else if (average_mark > 72){
                                letter_grade = "B";
                            }
            
                                else if (average_mark > 69){
                                    letter_grade = "B-";
                                }
            
                                else if (average_mark > 66){
                                    letter_grade = "C+";
                                }
            
                            else if (average_mark > 62){
                                letter_grade = "C";
                            }
            
                            else if (average_mark > 59){
                                letter_grade = "C-";
                            }
            
                        else if (average_mark > 56){
                            letter_grade ="D+";
                        }
            
                    if (average_mark > 52){
                        letter_grade = "D";
                    }
            
                if (average_mark > 49){
                    letter_grade = "D-";
                }
            
            if (average_mark <= 49){
                        letter_grade = "F";
            }
        
        return letter_grade;
    }
    /*Promotion method used to determine if student was promoted or not.
    If satement was used to make decision to determine promotion based on 
    overall percentage and age.*/
    //If the student’s age is equal or greater than 10 years then they will still be promoted even if their percentage is less than 50%.
    public static String Promotion (int age, double average_mark){
        
        String message;
        
        if (average_mark >= 50 || age >= 10){
            message = "Promoted to next class";                        
        }
        
        else {
            message = "Not promoted, repeating";
        }
        
        return message;
    }
}
