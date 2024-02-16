package main

import (
	"bufio"
	"fmt"
	"log"
	"os"
	"strconv"
	"strings"
)

type Task struct {
	title       string
	description string
	status      bool
}
type ListTask struct {
	tasks []Task
}

func main() {
	newTask1 := Task{
		title:       "Fiziks",
		description: "homework",
		status:      false,
	}
	newTask2 := Task{
		title:       "math",
		description: "homework",
		status:      false,
	}
	fullListTask := ListTask{[]Task{newTask1, newTask2}}
	reader := bufio.NewReader(os.Stdin)
	fmt.Println("Введите 1, чтобы вывести список")
	text, err := reader.ReadString('\n')
	if err != nil {
		log.Fatal(err)
	}
	text = strings.TrimSpace(text)
	number, err := strconv.Atoi(text)
	if err != nil {
		log.Fatal(err)
	}

	switch {
	case number == 1:
		for idx, task := range fullListTask.tasks {
			fmt.Printf("%d. Title: %s, Description: %s, Status: %t\n", idx+1, task.title, task.description, task.status)
		}
	}
}
