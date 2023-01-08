# Pipex
### Directions
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
```
$> ./pipex_bonus file1 "cmd1" "cmd2" "cmd3" ... cmdn file2
```
> 위의 결과값은 다음과 같습니다.
```
$> fil1 cmd1 | cmd2 | cmd3 ... | cmdn > file2
```
---
```
$> ./pipex_bonus here_doc LIMITER cmd cmd1 file
```
> 위의 결과값은 다음과 같습니다.
```
$> cmd << LIMITER | cmd1 >> file
```
### Development Report
