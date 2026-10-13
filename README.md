#include <iostream>
#include <iomanip>
int main() {
    int n;
    std::cin >> n;
    int* a = new int[n];
    for (int i = 0; i < n; i++) std::cin >> a[i];
    double sum = 0;
    int min = a[0], max = a[0], frost = 0;
    for (int i = 0; i < n; i++) {
        sum += a[i];
        if (a[i] < min) min = a[i];
        if (a[i] > max) max = a[i];
        if (a[i] < 0) frost++;
    }
    std::cout << std::fixed << std::setprecision(1) << sum / n << "\n";
    std::cout << min << " " << max << "\n";
    std::cout << frost << "\n";
    delete[] a;
    return 0;
}
