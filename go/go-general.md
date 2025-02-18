# General Golang Commands and Tips

## how to check the current dir
    pwd, err := os.Getwd()
    if err != nil {
        fmt.Println(err)
        os.Exit(1)
    }
