package main

import "fmt"

type haq struct {
	Name, Role, Portfolio string
	LanguageSpoken        []string
}

func main() {
	me := haq{
		Name: "haq",
		Role: "hacker, developer",
		LanguageSpoken: []string{"en_US"},
		Portfolio: "https://1hehaq.vercel.app",
	}

	fmt.Println("Thanks for stopping by!")
	fmt.Println("Check out my portfolio at:", me.Portfolio)
}
