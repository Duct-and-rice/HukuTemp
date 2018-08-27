require "rake"

task :update do
	version = ARGV.last
	puts "Update to #{version}\n"
	ARGV.slice(1,ARGV.size).each{|v| task v.to_sym do; end}

	sh "git add -A"
	sh "git config --local user.name Duct-and-rice"
	sh "git config --local user.email nikuinemitsubishi@gmail.com"
	sh "git commit -m '#{version}'"
	sh "git gc"
	sh "git push"
end