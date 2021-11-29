# Contact Manager

## Description
This is a basic contact manager that has a variety of features. It is written in Python and uses json files to store the data.
Configuration is done in the config.txt file.

## Commands
### add
Will add a contact to the contact list. It will prompt the user for the contact's name, phone number, and email address etc.
Usage:
    add

### remove [contact]
Will remove a contact from the contact list.
#### Parameters
    contact: Any identifier of the contact to be removed (eg. id, name, phone number, email address, etc.)

    Note: If the contact is not found, the command will not be executed.

### edit [contact]
Will edit a contact from the contact list. Will prompt for new values for the contact.
#### Parameters
    contact: Any identifier of the contact to be edited (eg. id, name, phone number, email address, etc.)

    Note: If the contact is not found, the command will not be executed.

### list
#### sub-commands
    - contacts
        Will list all the contacts in the contact list.
    - groups
        Will list all the groups in the contact list.

### search [contact]
Will search for contacts in the contact list. This is a wildcard search for all fields.
#### Parameters
    contact: Any identifier of the contacts to be searched (eg. id, name, phone number, email address, etc.)

### group
#### sub-commands
    - add [group] [contact]
        Will add a contact to a group.
    - remove [group] [contact]
        Will remove a contact from a group.

### note [contact]
Will add or edit the note for a contact.
#### Parameters
    contact: Any identifier of the contact to be edited (eg. id, name, phone number, email address, etc.)

    Note: If the contact is not found, the command will not be executed.

### commands [filename]
Will read and execute commands from a file.
#### Parameters
    filename: The name of the file to be read.
##### Example file 'cmds.txt'
add
name joe
phone 555-555-5555
add
name jane is a very long name
phone 555-555-5556
notes this is a note
remove jane is a very long name

### save
Will save the contact list to the default file.


### load [filename]
Will load the contact list from a file.
#### Parameters
    filename: The name of the file to load the contact list from.

    Note: If the file is not found, the command will not be executed.

### export [filename]
Will export the contact list to a file. Will also prompt to load from this file on next launch.
#### Parameters
    filename: The name of the file to export the contact list to.

    Note: If the file is not found, the command will not be executed.

### exit
Will exit the program. Will prompt to save the contact list before exiting unless always_save_on_exit is set to true in the config.txt file.

### help
Will display a help message with all the commands.

### fix
Will delete any duplicate contacts and emoty groups/companies.

### info
Will display number of contacts, groups, and companies. Will also display the number of contacts in each group and company.

### about
Will display information about the program.

## Contact Fields
### id
A unique identifier for the contact generated by the program on creation.
### name
The name of the contact.
### phone
The phone number of the contact.
### email
The email address of the contact.
### company
The company of the contact.
### groups
The groups of the contact.
### notes
Any notes for the contact.

## Configuration
Changes must be made in the config.txt file.
### always_save_on_exit
If set to true, the contact list will be saved before exiting without prompting.
### contacts_file
The name of the file to load the contact list from.
### splash_screen
If set to true, the splash screen will be displayed on startup.
### Example File
always_save_on_exit=true
contacts_file=contacts.json
splash_screen=true