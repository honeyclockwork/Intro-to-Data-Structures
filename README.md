# Intro-to-Data-Structures
Do not Copy any of the work that is going to be shown in this file. Copyright 2023.


#include <iostream>
#include <string>
#include "LabPrinter.h"
using namespace std;

void CallFunctionNamed(LabPrinter& printer, string functionName) {
    
    if (functionName == "Print2Plus2") {
        printer.Print2Plus2();
    } 
    else if (functionName == "PrintSecret") {
        printer.PrintSecret();
    } 
    else {
        cout << "Unknown function: " << functionName << endl;
    }
}

    


int main (int argc, char *argv[]) {
   LabPrinter printer("abc");
   
   // Step 1:
   // Uncomment the block below and submit code for grading. Note that the
   // submission passes the "Compare output" test, but fails each unit test.
   
  
   
    
   // After completing step 1:
   // Remove lines of code from step 1 and implement the CallFunctionNamed
   // function above main().
   CallFunctionNamed(printer, "Print2Plus2");
   CallFunctionNamed(printer, "PrintPlus2");
   CallFunctionNamed(printer, "PrintSecret");
    
   return(0);
}











#ifndef LABPRINTER_H
#define LABPRINTER_H
#include <iostream>
#include <string>

class LabPrinter {
protected:
   const std::string secret;

public:
   LabPrinter(std::string secretStringValue) : secret(secretStringValue) {
   }
   
   virtual void Print2Plus2() {
      using namespace std;
      cout << "2 + 2 = 4" << endl;
   }
   
   virtual void PrintSecret() {
      using namespace std;
      cout << "Secret string: \"" << secret << "\"" << endl;
   }
};

#endif
