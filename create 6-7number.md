**Задача 6**

#!/bin/bash

check() {
	local file=$1
	local ext=${file##*.}

	echo "Проверка: $file с расширением: .$ext"
	
	case $ext in
		c)
			if head -n 1 "$file" | grep -q '^\s*//' || head -n 1 "$file" | grep -q '^\s*/\*'; then
				echo "$file: Есть комментарий."
			else
				echo "$file: Нет комментария."
			fi
			;;
		js)
			if head -n 1 "$file" | grep -q '^\s*//'; then
				echo "$file: Есть комментарий."
			else
				echo "$file: Нет комментария."
			fi
			;;
		py)
			if head -n 1 "$file" | grep -q '^\s*#'; then
				echo "$file: Есть комментарий."
			else
				echo "$file: Нет комментария."
			fi
			;;
		*)
			echo "$file: Неподдерживаемый формат."
			;;
	esac
}


if [[ $# -ne 1 ]]; then
	echo "Использование: $0 <имя_файла>."
	exit 1
fi

if [[ -f $1 ]]; then
	check "$1"
else
	echo "Файл $file не найден."
	exit 1
fi

![image](https://github.com/user-attachments/assets/9d3e47cf-f6d7-40b6-a46c-8d1a0723880b)


**Задача 7**

#!/bin/bash

if [[ $# -ne 1 ]]; then
	echo "Использование: $0 /путь/к/каталогу."
	exit 1
fi

directory=$1

if [[ ! -d $directory ]]; then
	echo "Ошибка: каталог $directory не найден."
	exit 1
fi

declare -A file_hashes

while IFS= read -r -d '' file; do
	hash=$(sha256sum "$file" | awk '{ print $1 }')
	file_hashes["$hash"]+="file"$'\n'
done < <(find "$directory" -type f -print0)

found_duplicates=false

for hash in "${!file_hashes[@]}"; do
	files="${file_hashes[$hash]}"
	files_count=$(echo -e "files" | wc -l)


	if [[ $files_count -gt 1 ]]; then
		found_duplicates=true
		echo "Найдены дубликаты:"
		echo -e "$files"
	fi
done

if ! $found_duplicates; then
	echo "Дубликатов не найдено."
	exit 1
fi

![image](https://github.com/user-attachments/assets/188b4384-aae5-47eb-b0a8-6053b3e8f569)









