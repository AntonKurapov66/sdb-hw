# Домашнее задание к занятию "`Базы данных`" - `Курапов Антон`

## Задание 1
Опишите не менее семи таблиц, из которых состоит база данных:

* какие данные хранятся в этих таблицах;
* какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

## Сотрудники:(
	* id, primary_key , serial
	* фамилия, varchar(50)
	* имя, varchar(50) 
	* отчество, varchar(50) 
	* id должности, внешний ключ, integer
	* id структруного подразделения, внешний ключ, integer
	* дата найма, DATE )

## Подразделения:(
	* id, primary_key , serial
	* название подразделения, varchar(50)
	* id типа подразделения, внешний ключ, integer
	* id филиала, внешний ключ, integer )
 
## Тип подразделения:(
	* id, primary_key , serial
	* название типа , varchar(50)

## Должности:(
	* id, primary_key , serial
	* название должности, varchar(50) )

## Филиалы компании:(
	* id, primary_key , serial
	* адрес филиала, varchar(50) )

## Проекты:(
	* id, primary_key , serial
	* описание проекта, json )

## Оклады:(
	* id, primary_key , serial
	* сумма оклада, money
	* id должности, внешний ключ, integer
	* id проекта, внешний ключ, integer )

## Принадлежность к проекту:(
	* id сотрудника, внешний ключ, integer
	* id проекта, внешний ключ, integer )
