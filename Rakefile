# Vim utils
# 
module VimUtils
	class << self
		def root_dir
			@root_dir || File.expand_path('~')
		end

		def link_dot_vimrc
			source = File.expand_path('../dotvimrc', __FILE__)
			target = File.expand_path('.vimrc', root_dir)
			File.symlink(source, target)
		end
	end
end

namespace :vim do
	desc "Link .vimrc into users home folder"
	task :link_vimrc do
		::VimUtils.link_dot_vimrc
	end
end

