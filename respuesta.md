Escribiremos las respuestas desde la pregunta 35 hasta la 68

Pregunta 35. La diferencia esencial entre las dos formas literales de cadenas (comillas simples o dobles) es que las comillas dobles permiten secuencias de escape, mientras que las comillas simples no.
Un literal de cadena creado por comillas simples no admite la interpolación de cadenas y no escapa a las secuencias.
Pregunta 36. El %q es una forma alternativa de poner comillas simples en todo el texto
Pregunta 37. El %Q es una forma alternativa de poner comillas dobles en todo el texto
Pregunta 38. El resultado de c: "--4--\n--2--\n"
Pregunta 39. Resultado de c:  "--\#{a}--\n--\#{b}--\n"
Pregunta 40. s[0,2] => "he"    s[-1,1] => "o"   s[0,10] => "hello"
Pregunta 41. En g queda => "helloworld"
Pregunta 42. En e queda => "..."
Pregunta 43. El resultado es => "2 2 2 " 
Pregunta 44. Separa con comillas simples y con comas cada palabra de dentro de los corchetes
Pregunta 45. Separa con comillas dobles y ademas no interpreta terminaciones especiales, y ademas y separa por comas
Pregunta 46. Separa con comillas dobles y ademas interpreta correctamente como caracteres especiales, tambien separa con comas cada uno.
Pregunta 47. Contiene => [nil, nil, nil]
Pregunta 48. Contiene => [0, 0, 0] 
Pregunta 49. En b queda => [[1, 2], [3, 4]] 
Pregunta 50. En c queda  => [0, 2, 4] 
Pregunta 51. 2.6.5 :001 > a = ('a'..'e').to_a
			 => ["a", "b", "c", "d", "e"] 
			2.6.5 :002 > a[1,1]
			 => ["b"] 
			2.6.5 :003 > a[-2,2]
			 => ["d", "e"] 
			2.6.5 :004 > a[0..2]
			 => ["a", "b", "c"] 
			2.6.5 :005 > a[0...1]
			 => ["a"] 
			2.6.5 :006 > a[-2..-1]
			 => ["d", "e"] 
Pregunta 52.
			2.6.5 :007 > a
			=> ["a", "b", "c", "d", "e"] 
			2.6.5 :008 > a[0,2] = %w{A B}
			=> ["A", "B"] 
			2.6.5 :009 > a
			=> ["A", "B", "c", "d", "e"] 
			2.6.5 :010 > a[2..5] = %w{C D E}
			=> ["C", "D", "E"] 
			2.6.5 :011 > a
			=> ["A", "B", "C", "D", "E"] 
			2.6.5 :012 > a[0,0] = [1,2,3]
			=> [1, 2, 3] 
			2.6.5 :013 > a
			=> [1, 2, 3, "A", "B", "C", "D", "E"] 
			2.6.5 :014 > a[0,2] = []
			=> [] 
			2.6.5 :015 > a
			=> [3, "A", "B", "C", "D", "E"] 
			2.6.5 :016 > a[-1,1] = [ 'Z' ]
			=> ["Z"] 
			2.6.5 :017 > a
			=> [3, "A", "B", "C", "D", "Z"] 
			2.6.5 :018 > a[-2,2] = nil
			=> nil 
			2.6.5 :019 > a
			=> [3, "A", "B", "C", nil] 
 
Pregunta 53. 
			2.6.5 :020 > a = (1...4).to_a
			 => [1, 2, 3] 
			2.6.5 :021 > a = a + [4, 5]
			 => [1, 2, 3, 4, 5] 
			2.6.5 :022 > a += [[6, 7, 8]]
			 => [1, 2, 3, 4, 5, [6, 7, 8]] 
			2.6.5 :023 > a = a + 9
			Traceback (most recent call last):
			        5: from /home/usuario/.rvm/rubies/ruby-2.6.5/bin/irb:23:in `<main>'
			        4: from /home/usuario/.rvm/rubies/ruby-2.6.5/bin/irb:23:in `load'
			        3: from /home/usuario/.rvm/rubies/ruby-2.6.5/lib/ruby/gems/2.6.0/gems/irb-1.0.0/exe/irb:11:in `<top (required)>'
			        2: from (irb):23
			        1: from (irb):23:in `+'
			TypeError (no implicit conversion of Integer into Array)

Pregunta 54. 
			2.6.5 :001 > x = %w{a b c b a}
			 => ["a", "b", "c", "b", "a"] 
			2.6.5 :002 > x = x - %w{b c d}
			 => ["a", "a"] 

Pregunta 55. 
			2.6.5 :003 > z = [0]*8
			 => [0, 0, 0, 0, 0, 0, 0, 0] 
Pregunta 56. 
			2.6.5 :004 > a = []
			 => [] 
			2.6.5 :005 > a << 1
			 => [1] 
			2.6.5 :006 > a << 2 << 3
			 => [1, 2, 3] 
			2.6.5 :007 > a << [4, 5, 6]
			 => [1, 2, 3, [4, 5, 6]] 
			2.6.5 :008 > a.concat [7, 8]
			 => [1, 2, 3, [4, 5, 6], 7, 8] 

Pregunta 57. 
			2.6.5 :001 > a = [1, 1, 2, 2, 3, 3, 4]
			 => [1, 1, 2, 2, 3, 3, 4] 
			2.6.5 :002 > b = [5, 5, 4, 4, 3, 3, 2]
			 => [5, 5, 4, 4, 3, 3, 2] 
			2.6.5 :003 > c = a | b
			 => [1, 2, 3, 4, 5] 
			2.6.5 :004 > d = b | a
			 => [5, 4, 3, 2, 1] 
			2.6.5 :005 > e = a & b
			 => [2, 3, 4] 
			2.6.5 :006 > f = b & a
			 => [4, 3, 2] 

Pregunta 58.
			2.6.5 :001 > 1 = 1..10
			 => 1..10 
			2.6.5 :002 > a.class
			 => Range 
			2.6.5 :003 > a.to_a
			 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
			2.6.5 :004 > b = 1...10
			 => 1...10 
			2.6.5 :005 > b.to_a
			 => [1, 2, 3, 4, 5, 6, 7, 8, 9] 
			2.6.5 :006 > b.include? 10
			 => false 
			2.6.5 :007 > b.include? 8
			 => true 
			2.6.5 :008 > b.step(2) {|x| print "#{x} " }
			1 3 5 7 9  => 1...10 
			2.6.5 :009 > 1..3.to_a
			Traceback (most recent call last):
			        4: from /home/usuario/.rvm/rubies/ruby-2.6.5/bin/irb:23:in `<main>'
			        3: from /home/usuario/.rvm/rubies/ruby-2.6.5/bin/irb:23:in `load'
			        2: from /home/usuario/.rvm/rubies/ruby-2.6.5/lib/ruby/gems/2.6.0/gems/irb-1.0.0/exe/irb:11:in `<top (required)>'
			        1: from (irb):9
			NoMethodError (undefined method `to_a' for 3:Integer)
			Did you mean?  to_c
			               to_r
			               to_f
			               to_i
			               to_s

Pregunta 59.
			2.6.5 :011 > r = 0...100
			 => 0...100 
			2.6.5 :012 > r.member? 50
			 => true 
			2.6.5 :013 > r.include? 99.9 
			 => true 
			2.6.5 :014 > r.member? 99.9
			 => true 
Pregunta 60.
			2.6.5 :015 > true.class
			 => TrueClass 
			2.6.5 :016 > false.class
			 => FalseClass 
			2.6.5 :017 > puts "hello" if 0
			hello
			 => nil 
			2.6.5 :018 > puts "hello" if nil
			 => nil 
			2.6.5 :019 > puts "hello" if ""
			(irb):19: warning: string literal in condition
			hello
			 => nil 

Pregunta 61.
			2.6.5 :020 > x = :sym
			 => :sym 
			2.6.5 :021 > x.class
			 => Symbol 
			2.6.5 :022 > x == 'sym'
			 => false 
			2.6.5 :023 > x == :sym
			 => true 
			2.6.5 :024 > z = :'a long symbol'
			 => :"a long symbol" 
			2.6.5 :025 > z.class
			 => Symbol 
			2.6.5 :026 > x == 'sym'.to_sym
			 => true 
			2.6.5 :027 > x.to_s == 'sym'
			 => true 
Pregunta 62.
			2.6.5 :028 > s = "Ruby"
			 => "Ruby" 
			2.6.5 :029 > t = s
			 => "Ruby" 
			2.6.5 :030 > t[-1] = ""
			 => "" 
			2.6.5 :031 > print s
			Rub => nil 
			2.6.5 :032 > t = "Java"
			 => "Java" 
			2.6.5 :033 > print s, t
			RubJava => nil 
Pregunta 63.
			2.6.5 :034 > "%d %s" % [3, "rubies"]
			 => "3 rubies"

Pregunta 64.
			2.6.5 :035 > x, y = 4, 5
			 => [4, 5] 
			2.6.5 :036 > z = x > y ? x : y
			 => 5 
			2.6.5 :037 > x,y,z = [1,2,3]
			 => [1, 2, 3] 


Pregunta 65.
			2.6.5 :038 > x = { :a => 1, :b => 2}
			 => {:a=>1, :b=>2} 
			2.6.5 :039 > x.keys
			 => [:a, :b] 
			2.6.5 :040 > x.values
			 => [1, 2] 
			2.6.5 :041 > x[:c] = 3
			 => 3 
			2.6.5 :042 > x
			 => {:a=>1, :b=>2, :c=>3} 
			2.6.5 :043 > x.delete('a')
			 => nil 
			2.6.5 :044 > x
			 => {:a=>1, :b=>2, :c=>3} 
			2.6.5 :045 > x.delete(:a)
			 => 1 
			2.6.5 :046 > x
			 => {:b=>2, :c=>3} 
			2.6.5 :047 > x = { :a => 1, :b => 2, :c => 4 }
			 => {:a=>1, :b=>2, :c=>4} 
			2.6.5 :048 > x.delete_if { |k,v| v % 2 == 0 }
			 => {:a=>1} 
			2.6.5 :049 > x
			 => {:a=>1} 

Pregunta 66. La primera sentencia da como resultado vacio  => {}
La diferencia es que el primero pone el valor vacio, y la segunda pone el valor a nulo

Pregunta 67. Lo que retorna es 
				2.6.5 :001 > 'hello world, hello LPP'.scan /\w+/
				 => ["hello", "world", "hello", "LPP"] 
 

Pregunta 68. En el codigo hay que cambiar la condicion del while a !=
		while v != 0
		    u, v = v, u % v




Pregunta clase presencial:  [1,2,3]+[4,5,6]   => [1, 2, 3, 4, 5, 6]
