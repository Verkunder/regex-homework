# Регулярные выражения

| Задание                                                                           | Строка                                                                                                               | Решение                 |
| --------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | ----------------------- |
| 1.Выбрать все символы a,e,i,o                                                     | RegExr was created by gskinner.com, and is proudly hosted by Media Temple.                                           | /[aeio]/gm              |
| 2. Выбрать все символы которые не являются a,e,i,o                                | RegExr was created by gskinner.com, and is proudly hosted by Media Temple.                                           | /[^(aeio)]/gm           |
| 3. Выбрать все символы с g по s                                                   | Explore results with the Tools below.                                                                                | /[g-s]/g                |
| 4. Выбрать все символы не использую пред конструкцию                              | glib jocks vex dwarves!                                                                                              | /\D/gm                  |
| 5. Выбрать все слова, при этом не выбрав пробелы и знаки препинания               | RegExr was created by gskinner.com, and is proudly hosted by Media Temple.                                           | /\w/gm                  |
| 6. Выбрать всё что не является словами                                            | RegExr was created by gskinner.com, and is proudly hosted by Media Temple.                                           | /\W/gm                  |
| 7. Выбрать все цифры                                                              | +1-(444)-555-1234                                                                                                    | /\d/gm                  |
| 8. Выбрать всё что не является цифрами                                            | +1-(444)-555-1234                                                                                                    | /\D/gm                  |
| 9. Выбрать все пробелы без использования \W                                       | glib jocks vex dwarves!                                                                                              | / /gm                   |
| 10. Выбрать всё что не является пробелами                                         | glib jocks vex dwarves!                                                                                              | /[^ ]/gm                |
| 11. Выбрать первое слово RegExr в обоих строках                                   | RegExr was created by gskinner.com, and is proudly hosted by Media Temple. RegExr sells seashells                    | /^RegExr/gm             |
| 12. Выбрать последнее слово Temple в обоих строках                                | RegExr was created RegExr by gskinner.com, and is proudly hosted by Media Temple RegExr. RegExr sells Temple RegExr. | /Temple(?!.\*Temple)/gm |
| 13. Выбрать ha в любом количестве в обоих строках                                 | hahaha haa hah!                                                                                                      | /(ha)+/gm               |
| 14. Создать именованную группу                                                    | hahaha haa hah!                                                                                                      | /(ha)+/gm               |
| 15. Выбрать всё слова начинающиеся c b и после нее что то есть в любом количестве | b be bee beer beers                                                                                                  | /b\w+/gm                |
| 16. Выбрать всё слова начинающиеся c b                                            | b be bee beer beers                                                                                                  | /b\w\*/gm               |
| 17. Выбрать всё слова начинающиеся c b и после которых есть как минимум 2 символа | b be bee beer beers                                                                                                  | /b\w{2,}/gm             |
| 18. Выбрать всё слова начинающиеся c b и после которых есть как минимум 2 символа | color colour                                                                                                         | /colo(u\|\)r/gm         |
| 19. Выбрать cимволы после которого есть px                                        | 1pt 2px 3em 4px                                                                                                      | /((?=\dpx)\d)/gm        |
| 20. Выбрать cимволы после которого нет px                                         | 1pt 2px 3em 4px                                                                                                      | /((?!\dpx)\d)/gm        |
| 21. Составить RegExp для строки при которой пройдут все строки                    | 89281111111, 8-928-111-11-11, 8 928 111 11 11, 8(928) 111-11-11, +7 928 111 11 11                                    | Смотри ниже             |

## Решение задания 21

```
/((?=^(\+7))\+7 \d{3} \d{3} \d{2} \d{2}$|((?=^(8-))8-\d{3}-\d{3}-\d{2}-\d{2}$|((?=8 ))8 \d{3} \d{3} \d{2} \d{2}$))|((?=8\()8\(\d{3}\) \d{3}-\d{2}-\d{2}$)|\d+$/gm
```
