Матмодель работы
	Если один
		Выход
			просто 800
		Процент 
			Формула
				=ЕСЛИОШИБКА(ОКРУГЛ(G6*ЕСЛИ(G6<C6;0;ЕСЛИ(G6<D6;7%;10%)));0)
			Смысл {
				if выручка<микро
					0
				elsif выручка<минимум
					7%
				else
					10%
			}
		Премия
			Формула
				=ЕСЛИ(A20<СЕГОДНЯ();ЕСЛИ(G20>=E20;200)+ЕСЛИ(G20>=F20;200);"")+
				(СЧЁТЕСЛИМН
				(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!C:C");"Грязные")
				+СЧЁТЕСЛИМН
				(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!D:D");"Грязные")
				+СЧЁТЕСЛИМН
				(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!E:E");"Грязные / замочены")
				+СЧЁТЕСЛИМН
				(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!F:F");"Грязные")
				+СЧЁТЕСЛИМН
				(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!G:G");"Грязные")
				+СЧЁТЕСЛИМН
				(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!H:H");"Грязные"))*100"
			Смысл
				TODO: найти смысл, вытащить сокращенную до 4 importrange формулу. 
				//importrange тяжелый, найти обход через SQL
	Если двое
		Выход
			первому 
				800
			второму
				500
		Процент
			первому 
				Формула
					=ЕСЛИ(J17="стаж";ЕСЛИОШИБКА(ОКРУГЛ(СУММ(G16:G17)*ЕСЛИ(СУММ(G16:G17)<C16;0;ЕСЛИ(СУММ(G16:G17)<D16;5%;7%)));"");ЕСЛИОШИБКА(ОКРУГЛ(СУММ(G16:G17)*ЕСЛИ(СУММ(G16:G17)<C16;0;ЕСЛИ(СУММ(G16:G17)<D16;3,5%;5%)));""))"
			второму 
				Формула
					=ЕСЛИ(J16="стаж";ЕСЛИОШИБКА(ОКРУГЛ(СУММ(G16:G17)*ЕСЛИ(СУММ(G16:G17)<C16;0;ЕСЛИ(СУММ(G16:G17)<D16;5%;7%)));"");ЕСЛИОШИБКА(ОКРУГЛ(СУММ(G16:G17)*ЕСЛИ(СУММ(G16:G17)<C16;0;ЕСЛИ(СУММ(G16:G17)<D16;3,5%;5%)));""))"
		Премия
			Первому 
				Формула
					=ЕСЛИ(A20<СЕГОДНЯ();ЕСЛИ(G20>=E20;200)+ЕСЛИ(G20>=F20;200);"")+(
					СЧЁТЕСЛИМН(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!C:C");"Грязные")+
					СЧЁТЕСЛИМН(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!D:D");"Грязные")+
					СЧЁТЕСЛИМН(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!E:E");"Грязные / замочены")+
					СЧЁТЕСЛИМН(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!F:F");"Грязные")
					+СЧЁТЕСЛИМН(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!G:G");"Грязные")
					+СЧЁТЕСЛИМН(importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!B:B");СЖПРОБЕЛЫ(ДВССЫЛ("B1";ИСТИНА));importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");">"&A20;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!A:A");"<"&A22;importrange("14oppCH6rwdzdKGRr9cFZ6iwtz5T-1_uJOnAxnndMZrY";"Лог прихода на смену!H:H");"Грязные"))*100"
			Второму 
				Формула
					=ЕСЛИ(A18<СЕГОДНЯ();ЕСЛИ(J19<>"стаж";ЕСЛИ(СУММ(G18:G19)>=E18;200)+ЕСЛИ(СУММ(G18:G19)>=F18;200);0);"")"
