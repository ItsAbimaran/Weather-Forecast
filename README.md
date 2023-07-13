# Weather-Forecast
/* Name-Abinaya m
   Degree-BE.CST
   clg-Vivekanandha college of engineering 
   project-Weather forecast 
   language-C++
*/
   
   
#include <iostream>
#include<cstdlib>
using namespace std;
int intro ();
int first(string l);
int second (string l);
int intro ()
{
  char a;
  string loc;
  cout << "enter ur location:";
  cin >> loc;
  a = loc.at (0);
  if (a >= 'a' && a <= 'j')
    {
      first(loc);
    }
  else if (a >= 'k' && a <= 'u')
    {
      second (loc);
    }
  else if (a >= 'v' && a <= 'z')
    {
      second (loc);
    }
    return 0;

}

int first(string l)
{
  int temp = rand () % 56;
  int hum, rain,day;
  cout<<"1.today"<<endl<<"2.tomorrow"<<endl<<"3.yesterday"<<endl;
  cout<<"for which day u need an report:";
  cin>>day;
  if (temp <= 20)
    {
      hum = rand () % 50;
      rain = rand () % 20;
      cout << "location:" << l<<endl;
      cout << "temperature:" << temp << "c" << endl;
      cout << "the percentage of humidity :" << hum <<"%"<< endl;
      cout << "chance of rain/cloudy:" << rain<<"%"<< endl;
      cout << "the weather is normal" << endl;
    }
  else if (temp >= 20)
    {
      hum = rand () % 25;
      rain = rand () % 10;
      cout << "location:" << l<<endl;
      cout << "the percentage of temperature:" << temp << "c" << endl;
      cout << "the percentage of humidity :" << hum <<"%"<< endl;
      cout << "chance of rain/cloudy:" << rain<<"%" << endl;
      cout << "the weather is hot" << endl;
    }
  return 0;
}

int second (string l)
{
  int day;
  int temp = rand () % -273;
  int hum, rain;
  cout<<"1.today"<<endl<<"2.tomorrow"<<endl<<"3.yesterday"<<endl;
  cout<<"for which day u need an report:";
  cin>>day;
  if (temp <= -273)
    {
      hum = rand () % 50;
      rain = rand () % 90;
      cout << "location:" << l << endl;
      cout << "the temperature:" << temp << "c" << endl;
      cout << "the percentage of humidity :" << hum<<"%" << endl;
      cout << "chance of rain/cloudy:" << rain<<"%"<< endl;
      cout << "the weather is normal" << endl;
    }

  else if (temp >= -273)
    {
      hum = rand () % 75;
      rain = rand () % -273;
      cout << "location:" << l << endl;
      cout << "the temperature:" << temp << "c" << endl;
      cout << "the percentage of humidity :" << hum<<"%" << endl;
      cout << "chance of rain/cloudy:" << rain<<"%"<< endl;
      cout << "the weather is hot" << endl;
    }
  return 0;
}

int main ()
{
  char check;
  cout<<"|~|~|~|~|~|~WEATHER FORECAST IN C++|~|~|~|~|~|~"<<endl;
  intro();
  cout << "do you want to check forecast again...?(y/n)" << endl;
  cin >> check;
  while(check == 'y')
    {
      intro ();

    }
  cout << "thank you....!" << endl;


  return 0;
}
