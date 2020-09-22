<div align="center">

## C\+\+ File I/O Examples


</div>

### Description

This demonstrates an example of C++'s fstream File I/O. Very simple; the basic stuff for beginners to learn from. If you would like to see how to do something more in the direction this code leads, comment on (and rate) it telling me what specifically you want to see and I'll be glad to suffice.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[\*LuckY\*](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/lucky.md)
**Level**          |Beginner
**User Rating**    |4.2 (59 globes from 14 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Files](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files__3-2.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/lucky-c-file-i-o-examples__3-930/archive/master.zip)





### Source Code

```
//
// lucky760@yahoo.com
//
#include <fstream>
const char *FILENAME = "FILE.txt";
int main() {
	//create output object associated w/ file
	ofstream fout(FILENAME);
	cout << "Enter your secret password: ";
	char str[60];
	cin >> str;
	//write to file
	fout << "This is your secret password. Don't give it to anyone!\n";
	fout << str;
	//close file
	fout.close();
	cout << endl;
	ifstream fin(FILENAME);
	char ch;
	while (fin.get(ch))
		cout << ch;
	fin.close();
	return 0;
}
```

