# Ruby-Project-
require "./methods.rb"

reqfile = Hash.new(0) 

File.open('Users/alexandraespinosa/Downloads/ApacheLogs',r) do 

	f.each do |line|

	if line.ruby_safeguard 

		next 

	end


	find_rfile = line[/[a-zA-Z0-9]+\.[a-zA-Z1-9]+/]

	reqfile[find_rfile] += 1

	end

end

sorted = reqfile.sort {|k,v| v[1]. to_i <=> k[1].to_i }.to_h 
max_file = sorted.first 
puts "The most requested file is #{max_file[0]} with #{min[1]} request"

puts "----------------------------------------------------------------"

min_file = sorted.min_by(&:last)

put "The least requested file is #{min_file[0]} with #{min[1]} request"



