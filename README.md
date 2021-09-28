# cpp-things

## BG & FG colors

```cpp
void color(int fg, int bg)
{
    HANDLE H = GetStdHandle(STD_OUTPUT_HANDLE);
    SetConsoleTextAttribute(H, bg * 16 + fg);
}
```
Default colors: `color(15, 0);`

Colors:

0: Black/Noir<br>
1: Dark Blue/Bleu Foncé<br>
2: Green/Vert<br>
3: Blue-Grey/Bleu-Gris<br>
4: Marron<br>
5: Purple/Violet<br>
6: kaki<br>
7: Light Grey/Gris Clair<br>
8: Grey/Gris<br>
9: Blue/Bleu<br>
10: Neon Green/Vert Fluo<br>
11: Turquoise<br>
12: Red/Rouge<br>
13: Neon Pink/Rose Fluo<br>
14: Neon Yellow/Jaune Fluo<br>
15: White/Blanc<br>

=================================================================<br>
## Put Ascii

http://patorjk.com/software/taag/#p=display&f=Big%20Money-nw&t=Ascii

```cpp
std::cout << R"(
 $$$$$$\                      $$\ $$\ 
$$  __$$\                     \__|\__|
$$ /  $$ | $$$$$$$\  $$$$$$$\ $$\ $$\ 
$$$$$$$$ |$$  _____|$$  _____|$$ |$$ |
$$  __$$ |\$$$$$$\  $$ /      $$ |$$ |
$$ |  $$ | \____$$\ $$ |      $$ |$$ |
$$ |  $$ |$$$$$$$  |\$$$$$$$\ $$ |$$ |
\__|  \__|\_______/  \_______|\__|\__|
)" << std::endl;
```
<br>
=================================================================<br>

## Fuck Curl => CPR ("Curl Wrapper") is better

[CPR](https://github.com/libcpr/cpr)

<br>
=================================================================<br>

## See your exe name

```cpp
#include <iostream>
#include <boost/dll.hpp> //Debug&Release => Only x86
#include <windows.h>

void main() {
    SetConsoleOutputCP(CP_UTF8);
    std::string name = boost::dll::program_location().filename().string();
	std::cout << name << std::endl;
    system("pause");
}
```
<br>
=================================================================<br>

## Check the content of a string

```cpp
std::string a = "Dick Head";
if (a.find("Head") != std::string::npos) {
std::cout << "Found" << std::endl;
} else {
std::cout << "Not Found" << std::endl;
}
```

<br>
=================================================================<br>

# Get Screen Size

```cpp
#include <iostream>
#include <Windows.h>

int main()
{
    std::cout << "Hello World!\n" << GetSystemMetrics(SM_CXSCREEN) << "x" << GetSystemMetrics(SM_CYSCREEN) << std::endl;
}
```
