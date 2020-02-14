<p align="center">
	<img width="130px;" src="https://raw.githubusercontent.com/iwillenshofer/resources/main/images/42_logo_black.svg" align="center" alt="42" />&nbsp;&nbsp;&nbsp;
	<img width="130px" src="https://raw.githubusercontent.com/iwillenshofer/resources/main/achievements/get_next_line.png" align="center" alt="get_next_line" />
	<h1 align="center">get_next_line</h1>
</p>
<p align="center">
	<img src="https://img.shields.io/badge/Success-100/100_✓-gray.svg?colorA=61c265&colorB=4CAF50&style=for-the-badge">
	<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black">
	<img src="https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=apple&logoColor=white">
</p>

<p align="center">
	<b><i>Development repository for the 42cursus get_next_line project @ 42 São Paulo</i></b><br>
</p>

<p align="center">
	<img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/iwillenshofer/get_next_line?color=blueviolet" />
	<img alt="GitHub top language" src="https://img.shields.io/github/languages/top/iwillenshofer/get_next_line?color=blue" />
	<img alt="GitHub top language" src="https://img.shields.io/github/commit-activity/t/iwillenshofer/get_next_line?color=brightgreen" />
	<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/iwillenshofer/get_next_line?color=brightgreen" />
</p>
<br>

> _May it be a file, stdin, or even later a network connection, you will always need a way to read content line by line. It is time to start working on this function, which will be essential for your future projects._



<br>

<p align="center">
	<table>
		<tr>
			<td><b>Est. Time</b></td>
			<td><b>Skills</b></td>
			<td><b>Allowed Functions</b></td>
			<td><b>Difficulty</b></td>
		</tr>
		<tr>
			<td valign="top">70 hours</td>
			<td valign="top">
<img src="https://img.shields.io/badge/Algorithms & AI-555">
<img src="https://img.shields.io/badge/Unix-555">
<img src="https://img.shields.io/badge/Rigor-555">
			</td>
			<td valign="top">
				<img src="https://img.shields.io/badge/read()-lightgrey">
				<img src="https://img.shields.io/badge/malloc()-lightgrey">
				<img src="https://img.shields.io/badge/free()-lightgrey">
			</td>
			<td valign="top"> 882 XP</td>
		</tr>
	</table>
</p>

<br>


### Usage
```bash
# create a main file.
$ gcc get_next_line.c get_next_line_utils.c main.c -D BUFFER_SIZE=<size>
$ ./a.out
```

#### Example of main() file
```c
#include <stdio.h>
#include <fcntl.h>
#include "get_next_line.h"

int	main(void)
{
	char	*line;
	int		ret;
	int		i;
	int		fd;

	fd = open("main.c", O_RDONLY);
	line = NULL;
	while ((ret = get_next_line(fd, &line)))
	{
		printf("%s\n", line);
		free(line);
	}
	close(fd);
}
```

### Functions Included

|name					|prototype																	|
|---					|---																		|
|	get_next_line				|	int		get_next_line(int fd, char **line); |