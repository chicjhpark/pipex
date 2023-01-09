# Pipex
```
$> make
$> make bonus
```
![pipex_directions](https://user-images.githubusercontent.com/69841779/211208419-beb697c3-2a5c-4e24-af3f-3a1c2ff29b39.gif)
```
$> ./pipex file1 "cmd1" "cmd2" file2
```
> 위의 결과값은 다음과 같습니다.
```
$> < file1 cmd1 | cmd2 > file2
```
---
### Multiple Pipes
![ezgif-5-70ede36506](https://user-images.githubusercontent.com/69841779/211271522-60c5263f-022f-468f-95f4-7d4348930282.gif)
```
$> ./pipex_bonus file1 "cmd1" "cmd2" "cmd3" ... cmdn file2
```
> 위의 결과값은 다음과 같습니다.
```
$> < fil1 cmd1 | cmd2 | cmd3 ... | cmdn > file2
```
---
### Heredoc
![ezgif-5-6361282501](https://user-images.githubusercontent.com/69841779/211270334-6b072558-5598-4f24-933f-c27914b9540e.gif)
```
$> ./pipex_bonus here_doc LIMITER cmd cmd1 file
```
> 위의 결과값은 다음과 같습니다.
```
$> cmd << LIMITER | cmd1 >> file
```
### Development Report
