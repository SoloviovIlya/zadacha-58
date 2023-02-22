//Задайте две матрицы. Напишите программу, которая будет находить произведение двух матриц.
//Например, даны 2 матрицы:
//2 4 | 3 4
//3 2 | 3 3
//Результирующая матрица будет:
//18 20
//15 18

Console.WriteLine("Введите количество строк первой матрицы: ");

int m = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("Введите количество столбцов первой матрицы и строк второй матрицы: ");

int n = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("Введите количество столбцов второй матрицы: ");

int k = Convert.ToInt32(Console.ReadLine());

int[,] a = new int[m,n];

int [,] b = new int[n,k];

Console.WriteLine("Первая матрица: ");

Console.Write(Environment.NewLine + Environment.NewLine);

for (int i = 0; i < m;i++)

{

    for (int j =0; j<n; j++)
    
    {
    
        a[i,j] = new Random().Next(0,100);
        
        Console.Write(string.Format("{0} ", a[i, j]));
        
    }
    
    Console.Write(Environment.NewLine + Environment.NewLine);
    
}

Console.WriteLine("Вторая матрица: ");

Console.Write(Environment.NewLine + Environment.NewLine);

for (int i = 0; i < n;i++)

{

    for (int j =0; j<k; j++)
    
    {
    
        b[i,j] = new Random().Next(0,100);
        
        Console.Write(string.Format("{0} ", b[i, j]));
        
    }
    
    Console.Write(Environment.NewLine + Environment.NewLine);
    
}

int[,] c = new int[m,k];

for (int i =0;i<m;i++)

{

    int sum =0;
    
    for (int p=0;p<k;p++)
    
    {
    
        for (int j=0;j<n;j++)
        
        {
           sum = sum + a[i,j]*b[j,p];
        }
        
        c[i,p] = sum;
        
    }
    
}

Console.WriteLine("Матрица произведения: ");

Console.Write(Environment.NewLine + Environment.NewLine);

for (int i = 0; i < m;i++)

{

    for (int j =0; j<k; j++)
    
    {
        Console.Write(string.Format("{0} ", c[i, j]));
    }
    
    Console.Write(Environment.NewLine + Environment.NewLine);
    
}
