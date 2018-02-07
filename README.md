# 236A---Boy-or-Girl

#include <iostream>
using namespace std;

int arr[26];

int main()
{
	string w = "abcdefghijklmnopqrstuvwxyz";
	string name;
	cin >> name;
	
  int sum =0;
  
	for (int i = 0; i < name.size(); i++)
	{
		if (w.find(name[i]) != std::string::npos)
			arr[w.find(name[i])] = 1;
	}
	for (int i = 0; i < 26; i++)
		sum += arr[i];
	
	if (sum % 2 == 1)
		cout << "IGNORE HIM!";
	else
		cout << "CHAT WITH HER!";
  
  return 0;
}
