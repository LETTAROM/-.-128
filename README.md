# -.-128
Специализация шаблона класса. #128
template<typename T>
class Printer
{
public:
	void Print(T value)
	{
		cout << value << endl;
	}
};


template<>
class Printer<string>//с помощью спец-ции шаблона м.запретить исполь-е типа стринг
	//с Printer если без описания реал-ии внутри
{
public:
	void Print(string value)//напишем свою особую реал-ю метода Print
	{
		cout <<"____"<< value <<"___"<< endl;
	}
};
int main()
{
	Printer<int> p;
	p.Print(545);
	Printer<string>st;
	st.Print("Hello Sveta!!");

	return 0;
}



