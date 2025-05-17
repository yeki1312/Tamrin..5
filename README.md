# Tamrin..5
using System;

class Program
{
    // تابع بازگشتی برای محاسبه حاصل‌ضرب دو عدد
    static int Multiply(int a, int b)
    {
        // شرایط پایه: اگر b برابر 0 باشد، حاصل‌ضرب برابر 0 است
        if (b == 0)
            return 0;

        // بازگشتی: حاصل‌ضرب a و b برابر است با a + حاصل‌ضرب a و (b-1)
        return a + Multiply(a, b - 1);
    }

    static void Main()
    {
        // دریافت ورودی از کاربر
        Console.Write("لطفاً عدد اول (a) را وارد کنید: ");
        int a = int.Parse(Console.ReadLine());

        Console.Write("لطفاً عدد دوم (b) را وارد کنید: ");
        int b = int.Parse(Console.ReadLine());

        // محاسبه حاصل‌ضرب با استفاده از تابع بازگشتی
        int result = Multiply(a, b);

        // نمایش نتیجه
        Console.WriteLine($"حاصل‌ضرب {a} و {b} برابر است با: {result}");
    }
}

