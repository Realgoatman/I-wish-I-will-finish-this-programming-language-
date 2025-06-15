# I-wish-I-will-finish-this-programming-language
Please encourage me to finish this project

---

I don't really have a name for this programming language yet, but I just called it `proglang` for now, its main goals are:\
1."lightweight"

I can only think of example, because that's what I have

---

and here it is:

	#void([Why did I feel like there is a lot of noise]);
	$left() : 0;
	$operand() : [];
	$right() : 0;
	$result() : 0;
	$line() : 0;
	#goto($skip_fnc());
	
	#label($add());
		$result() : $left() + $right();
	#jump($line());
	
	#label($sub());
		$result() : $left() - $right();
	#jump($line());
	
	#label($mul());
		$result() : $left() * $right();
	#jump($line());
	
	#label($div());
		$result() : $left() / $right();
	#jump($line());
	
	#label($mod());
		$result() : $left() % $right();
	#jump($line());
	
	#label($skip_fnc());
	#put([Enter an integer for the left side of equation: ]);
	$left() : #get($int()); a 
	
	#void([if the left side is invalid]);
	#void([#invalid(...) return int 0 if valid, otherwise 1]);
	!when(#invalid($left(), $int()))
	{
		#put([The left side may now be 0.n]);
		$left() : 0;
	};
	
	#void([loop until operand is valid]);
	!loop(#invalidchar($operand(), [+-*/%]))
	{
		#put([Enter a character for the operand of equation: ]);
		$operand() : #get($str());
	};
	
	#put([Enter an integer for the right side of equation: ]);
	$right() : #get($int());
	
	#void([if the left side is invalid]);
	!when(#invalid($right(), $int()))
	{
		#put([The right side may now be 0.n]);
		$right() : 0;
	};
	
	#void([This program can be optimise more,]);
	#void([but this just meant to show all features of this language]);
	#put([Result: ]);
	
	!when($operand() = [+])
	{
		$line() : #line();
		$line() : $line() + 3;
		#goto($add());
	};
	
	!when($operand() = [-])
	{
		$line() : #line();
		$line() : $line() + 3;
		#goto($sub());
	};

	!when($operand() = [*])
	{
		$line() : #line();
		$line() : $line() + 3;
		#goto($mul());
	};
	
	!when($operand() = [/])
	{
		$line() : #line();
		$line() : $line() + 3;
		#goto($div());
	};
	
	!when($operand() = [%])
	{
		$line() : #line();
		$line() : $line() + 3;
		#goto($mod());
	};
 	#put($result());
 	#put([.n]);
  	#halt();

---

Currently, the language interpreter will be impermented in Lua, and in the future, it will I will also made one in C
