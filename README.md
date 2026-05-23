


# 🔧 Решение ошибки `detail_prop_types.vdata_c not found` в Hammer

## Русский

### Описание проблемы

При работе в Hammer (редактор карт для игр на движке Source 2, например, CS2) вы могли столкнуться с ошибкой:

```
detail_prop_types.vdata_c not found
```

Она возникает, когда игра или инструментарий не могут найти или правильно прочитать файл `detail_prop_types.vdata_c`. Это приводит к невозможности использовать детальные пропсы (траву, камни и т.п.) или даже к вылету редактора.

### Причина

В некоторых сборках SDK или после обновлений игр этот файл отсутствует, повреждён или имеет неверный формат. Обычно он должен лежать в папке `scripts/` и содержать определения типов детальных пропсов.

### Решение

В этом репозитории вы найдёте рабочий файл `detail_prop_types.vdata_c`, который восстанавливает функциональность.

#### Установка

1. Скачайте файл `detail_prop_types.vdata_c` из репозитория.
2. Поместите его в папку `scripts/` вашей конкретной игры (или в корневую папку SDK).  
   Примеры путей:
   - `Steam/steamapps/common/Counter-Strike Global Offensive/csgo_addons/название проекта/scripts`

3. Если папки `scripts` нет — создайте её.
4. Перезапустите Hammer.

После этого ошибка должна исчезнуть.

### Примечание

Если проблема сохраняется, проверьте права доступа к файлу и убедитесь, что в папке `scripts` нет других конфликтующих версий `detail_prop_types*`.

---

## English

### Problem Description

While working in Hammer (the map editor for Source 2 Engine games such as CS2), you may encounter the error:

```
detail_prop_types.vdata_c not found
```

This error occurs when the game or the tools cannot locate or correctly read the `detail_prop_types.vdata_c` file. As a result, you may be unable to place detail props (grass, rocks, etc.) or Hammer might crash.

### Cause

In some SDK builds or after game updates, this file is missing, corrupted, or has an incorrect format. Normally, it should be located in the `scripts/` folder and contain definitions for detail prop types.

### Solution

This repository provides a working `detail_prop_types.vdata_c` file that restores full functionality.

#### Installation

1. Download the `detail_prop_types.vdata_c` file from this repository.
2. Place it into the `scripts/` folder of your specific game (or the SDK root folder).  
   Example paths:
- `Steam/steamapps/common/Counter-Strike Global Offensive/csgo_addons/название проекта/scripts`
  
3. If the `scripts` folder does not exist — create it.
4. Restart Hammer.

The error should now be resolved.

### Note

If the problem persists, check the file’s read permissions and make sure there are no conflicting `detail_prop_types*` files inside the `scripts` folder.

