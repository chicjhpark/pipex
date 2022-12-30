# Pipex
### Introduction
- 유닉스의 동작 원리를 알아가는 프로그램입니다.
### Objectives
> 프로그램은 다음과 같이 실행될 것입니다.

    $> ./pipex file1 cmd1 cmd2 file2
> file1과 file2는 파일명이고, cmd1과 cmd2에는 쉘 명령어와 그에 대한 인자값이 들어갑니다.

> 프로그램의 동작 결과는 다음 명령줄을 쉘에서 실행할 때의 결과와 동일하여야 합니다.

    $> < file1 cmd1 | cmd2 > file2
### Examples
    $> ./pipex infile ``ls -l'' ``wc -l'' outfile

> 위의 명령줄은 “< infile ls -l | wc -l > outfile” 와 같이 동작하여야 합니다.

    $> ./pipex infile ``grep a1'' ``wc -w'' outfile
    
> 위의 명령줄은 “< infile grep a1 | wc -w > outfile” 와 같이 동작하여야 합니다.
### Bonus part
> 다중 파이프 구현하기

    $> ./pipex file1 cmd1 cmd2 cmd3 ... cmdn file2
> 위의 결과값은 다음과 같아야 합니다.

    $> < file1 cmd1 | cmd2 | cmd3 ... | cmdn > file2
> 첫 번째 인자값이 "here_doc" 일 경우 <<와 >> 구현하기

    $> ./pipex here_doc LIMITER cmd cmd1 file
> 위의 결과값은 다음과 같아야 합니다.

    $> cmd << LIMITER | cmd1 >> file
    

    
