# assignment2
void Persons:: removeper(string input2)
{
        Person *temp = head;
	Person *deltemp = head;

	if(head->getname() == input2){
		head = deltemp->next;
		cout << deltemp->getname() << "\n";
		delete deltemp;
		cout << "Removal Successful: " << input2 << "\n\n";
		return;
	}

	while(deltemp != NULL)
	{
		if(deltemp->getname() == input2)
		{
			temp->next = deltemp->next;
			cout << "Removal Successful squak: " << deltemp->getname() << "\n\n";
			delete deltemp;
		}

		temp = temp->next;
		deltemp = deltemp->next;
	}

		cout << "Patron removed!\n";
}
