#include <iostream>
#include <string>

using namespace std;

// تعريف هيكل لتمثيل المهمة
struct Task {
    string name;
    int hours;
};

int main() {
    const int SIZE = 3; // عدد المهام
    Task list[SIZE];
    int totalHours = 0;

    cout << "--- برنامج إدارة المهام اليومية ---" << endl;

    // حلقة لإدخال البيانات
    for (int i = 0; i < SIZE; i++) {
        cout << "أدخل اسم المهمة " << i + 1 << ": ";
        cin >> list[i].name;
        cout << "كم ساعة تحتاج لإنجازها؟ ";
        cin >> list[i].hours;
        totalHours += list[i].hours;
    }

    cout << "\n--- قائمة مهامك الحالية ---" << endl;
    for (int i = 0; i < SIZE; i++) {
        cout << "- " << list[i].name << " (" << list[i].hours << " ساعة)" << endl;
    }

    cout << "---------------------------" << endl;
    cout << "إجمالي الساعات المطلوبة: " << totalHours << " ساعة." << endl;

    return 0;
}
