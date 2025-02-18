## Enable dependency tracking by creating a go.mod File
    - go mod init example/module

## to run go application 
    - go run filename.go in your terminal

## range example
    numbers := []int{10, 20, 30, 40, 50}

    for index, value := range numbers {
        fmt.Printf("Index: %d, Value: %d\n", index, value)
    }

## manual extract value from array
- testBoxItemList := &[]itemsPackage.Item{item1, item2, item3}
- firstItem := (*testBoxItemList)[0]

- testBoxItemList := []itemsPackage.Item{item1, item2, item3}
- firstItem := testBoxItemList[0]
