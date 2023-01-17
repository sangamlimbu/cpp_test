**1. What will be the value of "x"?**
```cpp
int x=1;
{ int x=1; }
x += 1;
```

**2. What will be the value of "x"?**
```cpp
char *x = new char('1');
int y = 2;
x = (char *)&y;
```

**3. What will be the ouput of following**
```cpp
class A
{
	public:
	virtual void print(const string& name) { cout << "Name is: " << name << endl; }
};

class B : public A {};

int main()
{
	A a;
	a.print("Adam");
	
	B b; 
	b.print("Jack");
	return 0;
}
```

**4. What will be the output of following**
```cpp
class A
{
	public:
	void print(const string& name) { cout << "Name is: " << name << endl; }
	void print(const int age) { cout << "Age is: " << age << endl; }
};

int main()
{
	A a;
	a.print("Adam");
	a.print(20);
	return 0;
}
```

**5. Is the following code able to compile?**
```cpp
class A
{
	public:
	virtual void print(const string& name) { cout << "Public Name is: " << name << endl; }
	
	protected:
	virtual void print(const int age) { cout << "Protected Age is: " << age << endl; }
};

class B : public A {};

int main()
{
	B b;
	b.print("Jack");
	b.print(20);
	return 0;
}
```
> If Yes, what will be the output?

> If Not, why the above code won't compile?

**6. In below code will both line compile or give out error?**
```cpp
void *x; char *y;
x = y; //<== will this compile?
y = x; //<== will this compile?
```

**7. Difference between virtual function and pure virtual function?**

**8. What will be the value of a4.num in following code**
```cpp
class A
{
	public:
	void operator&(const A& a)
	{
		this->num = a.num;
	}
	void operator=(const A& a)
	{
		this->num -= a.num;
	}
	bool operator==(const A& a)
	{
		return (a.num == this->num ? true : false);
	}
	int 		num{0};
};

int main()
{
	A a1; A a2;
	a1.num = 20;
	a2.num = a1.num;
	cout << "Both are same: " << (a1 == a2 ? "true" : "false") << endl; //<== what will be the output of this?

	A a3; A a4;
	a3.num = 40;
	a4 = a3;
	cout << "Value of a4.num=" << a4.num << endl; //<== what will be the output of a4.num?
	return 0;
}
```

**9. What will be the value of x in two lines?**
```cpp
	int x=1;
	cout << "x=" << ++x << endl; //<== What will be x here?
	cout << "x=" << x++ << endl; //<== What will be x here?
```

**10. What will be the out of the following:**
```cpp
enum color {red, green, blue, yellow };
cout << red << " " << blue << " " << green << " " << yellow << endl; // <== What will be the output of this line?
```

**11. What will be the value of i?**
```cpp
int i;
int j=10;
i=(j++, j+100, 999+j);
cout << "i=" << i << endl;
```
