#include <stdio.h>

// ============= HUMAN NOTES FOR IF-ELSE IN C=========
// 1. if() - Single condition check
// 2. if-else - Two options (true/false)
// 3. if-else if-else - Multiple conditions (like menu options)
// 4. Nested if-else - if inside another if (like Russian doll)
// 5. Logical operators: &&(AND), ||(OR), !(NOT)
// =======================================================

int main() {
    
    int age, marks;
    char grade;
    
    printf("=== C IF-ELSE STUDY NOTES - Multiple Examples ===\n\n");
    
    // EXAMPLE 1: Simple IF statement
    printf("EXAMPLE 1 - Simple IF:\n");
    age = 20;
    if(age >= 18) {
        printf("✅ You can vote! Age = %d\n\n", age);
    }
    // Note: If condition false, nothing prints!
    
    // EXAMPLE 2: IF-ELSE (Two choices)
    printf("EXAMPLE 2 - IF-ELSE:\n");
    marks = 75;
    if(marks >= 60) {
        printf("🎉 PASS! Marks = %d\n", marks);
    } else {
        printf("❌ FAIL! Marks = %d, Study harder!\n", marks);
    }
    printf("\n");
    
    // EXAMPLE 3: IF-ELSE IF-ELSE (Multiple options - BEST FOR GRADES)
    printf("EXAMPLE 3 - IF-ELSE IF-ELSE (Grade System):\n");
    printf("Enter your marks (0-100): ");
    scanf("%d", &marks);
    
    if(marks >= 90) {
        grade = 'A';
        printf("🏆 Grade %c - Topper! 🎖️\n", grade);
    }
    else if(marks >= 80) {
        grade = 'B';
        printf("✅ Grade %c - Excellent! 👏\n", grade);
    }
    else if(marks >= 70) {
        grade = 'C';
        printf("👍 Grade %c - Good job! 💪\n", grade);
    }
    else if(marks >= 60) {
        grade = 'D';
        printf("📚 Grade %c - Just passed! Keep going 📖\n", grade);
    }
    else {
        grade = 'F';
        printf("😢 Grade %c - Better luck next time! Study more! 📚\n", grade);
    }
    printf("\n");
    
    // EXAMPLE 4: NESTED IF-ELSE (Condition inside condition)
    printf("EXAMPLE 4 - NESTED IF-ELSE:\n");
    age = 16;
    printf("Age check: %d\n", age);
    
    if(age >= 18) {
        printf("Adult! Can:\n");
        if(age >= 21) {
            printf("- Drink alcohol legally ✅\n");
        } else {
            printf("- Cannot drink yet ❌\n");
        }
    } else {
        printf("Minor! Cannot vote or drink ❌\n");
    }
    printf("\n");
    
    // EXAMPLE 5: Logical Operators (&&, ||, !)
    printf("EXAMPLE 5 - LOGICAL OPERATORS:\n");
    int math = 85, science = 45;
    
    // AND (&&) - BOTH true
    if(math >= 60 && science >= 60) {
        printf("✅ Perfect! Both subjects good!\n");
    } else {
        printf("⚠️ One subject weak - Science = %d\n", science);
    }
    
    // OR (||) - ANY ONE true
    if(math >= 60 || science >= 60) {
        printf("✅ At least one subject good! Math = %d\n", math);
    }
    
    // NOT (!) - Opposite
    if(!(science >= 60)) {
        printf("❌ Science needs improvement!\n");
    }
    
    printf("\n=== END OF IF-ELSE NOTES ===\n");
    printf("💡 Key Points:\n");
    printf("- Use == for equality, = for assignment\n");
    printf("- else if saves time vs many ifs\n");
    printf("- Nesting = conditions inside conditions\n");
    
    return 0;
}
