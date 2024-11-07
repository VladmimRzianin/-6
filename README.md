
//12

Console.Write("Введите строку S ");
string s = Console.ReadLine();

Console.Write("Введите число N ");
int n = int.Parse(Console.ReadLine());

if (n > 0)
{
    string result = string.Join(new string('*', n), s.ToCharArray());
    Console.WriteLine("Результат: " + result);
}
else
{
    Console.WriteLine("Число N должно быть больше 0 ");
}



//20
        
Console.Write("ввести целое число ");
string input = Console.ReadLine();

if (!string.IsNullOrEmpty(input) && int.TryParse(input, out int number) && number > 0)
{
    Console.WriteLine("цифры числа ");
    foreach (char i in input)
    {
        Console.WriteLine(i);
    }
}


//29
Console.Write("Введите строку S ");
string S = Console.ReadLine();

Console.Write("Введите строку A ");
string A = Console.ReadLine();

Console.Write("Введите символ C ");
char C = Console.ReadKey().KeyChar;

string result = S.Replace(C.ToString(), A + C);

Console.WriteLine("Результат: " + result);


//54

Console.Write("Введите строку: ");
string input = Console.ReadLine();

int vowelCount = CountVowels(input);

Console.WriteLine("количество гласных букв  " + vowelCount);

static int CountVowels(string input)
{
    char[] vowels = { 'а', 'е', 'ё', 'е', 'и', 'о', 'у', 'ы', 'э', 'ю', 'я',
                          'А', 'Е', 'Ё', 'И', 'О', 'У', 'Ы', 'Э', 'Ю', 'Я' };

  int count = 0;
    
  foreach (char ch in input)
    {
        if (Array.Exists(vowels, vowel => vowel == ch))
        {
            count++;
        }
    }

  return count;
}
