// 1. Multiplication of boundary elements of a 2D array (20x20)
int multiplyBoundaryElements(int arr[20][20]) {
    int product = 1;
    for (int i = 0; i < 20; i++) {
        for (int j = 0; j < 20; j++) {
            if (i == 0 || i == 19 || j == 0 || j == 19) {
                product *= arr[i][j];
            }
        }
    }
    return product;
}


// 2. Summation of boundary elements of a square 2D array (SxS)
int sumBoundaryElements(int arr[S][S], int size) {
    int sum = 0;
    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            if (i == 0 || i == size - 1 || j == 0 || j == size - 1) {
                sum += arr[i][j];
            }
        }
    }
    return sum;
}


// 3. Inserting a new element at the second position of an array
// (Assumes the array has enough capacity to hold the new element)

void insertAtSecondPosition(int arr[], int size, int newElement) {
    // Shift elements from the second position onwards to the right
    for (int i = size; i > 1; i--) { 
        arr[i] = arr[i - 1];
    }
    // Insert the new element at the second position (index 1)
    arr[1] = newElement;
}
