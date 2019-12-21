# XC16

A docker environment for building MPLAB X projects by XC16


### Installing


```
docker pull badinszky97/xc16_stable
```

## Running an empty tests

```
docker run -it badinszky97/xc16_stable
```

### Running the container with a project

This mounts your home folder into the container's "/myproject" folder. You can build there.

```
docker run -it -v ~:/myproject badinszky97/xc16_stable
```

### Building

You have to remake the makefiles.

```
/opt/microchip/mplabx/v3.40/mplab_ide/bin/prjMakefilesGenerator.sh /myproject/xx/a_project.X/@default
cd /myproject/xx/a_project.X/
make clean
make
```



## Author

* **Daniel Badinszky** - *Initial work* - [Github](https://github.com/badinszky97) [Gitlab](https://gitlab.com/badidani) 


## License

This project is licensed under the GNU License - see the [LICENSE](LICENSE) file for details

