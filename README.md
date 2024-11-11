#include <stdio.h>

int is_palindrome(int n) {
    int original = n, reversed = 0, remainder;
    
    // Reverse the number
    while (n != 0) {
        remainder = n % 10;
        reversed = reversed * 10 + remainder;
        n /= 10;
    }

    // Check if the original number is equal to its reversed version
    return original == reversed;
}

int main() {
    int num;

    // Test cases
    num = 12344321;
    printf("%d   %s\n", num, is_palindrome(num) ? "true" : "false");

    num = 0;
    printf("%d   %s\n", num, is_palindrome(num) ? "true" : "false");

    num = 123;
    printf("%d   %s\n", num, is_palindrome(num) ? "true" : "false");

    return 0;
}
