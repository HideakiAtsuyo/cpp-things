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
