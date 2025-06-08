funcsave () {
	local fn=$1 dir=${ZFUNC:-$HOME/.zsh/functions} 
	[[ -z $fn ]] && {
		echo "usage: funcsave <name>"
		return 1
	}
	command -v "$fn" > /dev/null || {
		echo "no such function: $fn"
		return 1
	}
	mkdir -p "$dir"
	which "$fn" >| "$dir/$fn"
	chmod +x "$dir/$fn"
	echo "saved $fn → $dir/$fn"
}
