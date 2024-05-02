import tkinter as tk
from tkinter import ttk, simpledialog, messagebox
from part1 import Employee, Event, Client
from part2 import Guest, Supplier, Venue


class EventManagementApp(tk.Tk):
    def __init__(self):
        super().__init__()
        self.title("Event Management System")
        self.geometry("600x400")

        self.notebook = ttk.Notebook(self)
        self.notebook.pack(fill=tk.BOTH, expand=True)

        self.employee_frame = EmployeeFrame(self.notebook)
        self.event_frame = EventFrame(self.notebook)
        self.client_frame = ClientFrame(self.notebook)
        self.guest_frame = GuestFrame(self.notebook)
        self.supplier_frame = SupplierFrame(self.notebook)
        self.venue_frame = VenueFrame(self.notebook)

        self.notebook.add(self.employee_frame, text="Employees")
        self.notebook.add(self.event_frame, text="Events")
        self.notebook.add(self.client_frame, text="Clients")
        self.notebook.add(self.guest_frame, text="Guests")
        self.notebook.add(self.supplier_frame, text="Suppliers")
        self.notebook.add(self.venue_frame, text="Venues")


class EmployeeFrame(tk.Frame):
    def __init__(self, parent):
        super().__init__(parent)
        self.parent = parent
        self.employees = []

        self.label = ttk.Label(self, text="Employee Management")
        self.label.pack()

        self.add_button = ttk.Button(self, text="Add Employee", command=self.add_employee)
        self.add_button.pack()

        self.delete_button = ttk.Button(self, text="Delete Employee", command=self.delete_employee)
        self.delete_button.pack()

        self.modify_button = ttk.Button(self, text="Modify Employee", command=self.modify_employee)
        self.modify_button.pack()

        self.display_button = ttk.Button(self, text="Display Employee Details", command=self.display_employee_details)
        self.display_button.pack()

    def add_employee(self):
        name = simpledialog.askstring("Employee Details", "Enter Name:")
        if name is not None:
            employee_id = simpledialog.askinteger("Employee Details", "Enter Employee ID:")
            department = simpledialog.askstring("Employee Details", "Enter Department:")
            job_title = simpledialog.askstring("Employee Details", "Enter Job Title:")
            basic_salary = simpledialog.askinteger("Employee Details", "Enter Basic Salary:")
            age = simpledialog.askinteger("Employee Details", "Enter Age:")
            date_of_birth = simpledialog.askstring("Employee Details", "Enter Date of Birth (YYYY-MM-DD):")
            passport_details = simpledialog.askstring("Employee Details", "Enter Passport Details:")

            employee = Employee(name, employee_id, department, job_title, basic_salary, age, date_of_birth,
                                passport_details)
            self.employees.append(employee)
            messagebox.showinfo("Success", "Employee added successfully.")

    def delete_employee(self):
        employee_id = simpledialog.askinteger("Employee ID", "Enter Employee ID to delete:")
        if employee_id is not None:
            for employee in self.employees:
                if employee.getEmployeeID() == employee_id:
                    self.employees.remove(employee)
                    messagebox.showinfo("Success", "Employee deleted successfully.")
                    return
            messagebox.showerror("Error", "Employee not found.")

    def modify_employee(self):
        employee_id = simpledialog.askinteger("Employee ID", "Enter Employee ID to modify:")
        if employee_id is not None:
            for employee in self.employees:
                if employee.getEmployeeID() == employee_id:
                    name = simpledialog.askstring("Employee Details", "Enter Name:", initialvalue=employee.getName())
                    if name is not None:
                        department = simpledialog.askstring("Employee Details", "Enter Department:",
                                                            initialvalue=employee.getDepartment())
                        job_title = simpledialog.askstring("Employee Details", "Enter Job Title:",
                                                           initialvalue=employee.getJobTitle())
                        basic_salary = simpledialog.askinteger("Employee Details", "Enter Basic Salary:",
                                                               initialvalue=employee.getBasicSalary())
                        age = simpledialog.askinteger("Employee Details", "Enter Age:", initialvalue=employee.getAge())
                        date_of_birth = simpledialog.askstring("Employee Details", "Enter Date of Birth (YYYY-MM-DD):",
                                                               initialvalue=employee.getDateOfBirth())
                        passport_details = simpledialog.askstring("Employee Details", "Enter Passport Details:",
                                                                  initialvalue=employee.getPassportDetails())

                        employee.setName(name)
                        employee.setDepartment(department)
                        employee.setJobTitle(job_title)
                        employee.setBasicSalary(basic_salary)
                        employee.setAge(age)
                        employee.setDateOfBirth(date_of_birth)
                        employee.setPassportDetails(passport_details)
                        messagebox.showinfo("Success", "Employee modified successfully.")
                        return
            messagebox.showerror("Error", "Employee not found.")

    def display_employee_details(self):
        employee_id = simpledialog.askinteger("Employee ID", "Enter Employee ID:")
        if employee_id is not None:
            for employee in self.employees:
                if employee.getEmployeeID() == employee_id:
                    messagebox.showinfo("Employee Details",
                                        f"Name: {employee.getName()}\nEmployee ID: {employee.getEmployeeID()}\nDepartment: {employee.getDepartment()}\nJob Title: {employee.getJobTitle()}\nBasic Salary: {employee.getBasicSalary()}\nAge: {employee.getAge()}\nDate of Birth: {employee.getDateOfBirth()}\nPassport Details: {employee.getPassportDetails()}")
                    return
            messagebox.showerror("Error", "Employee not found.")


class EventFrame(tk.Frame):
    def __init__(self, parent):
        super().__init__(parent)
        self.parent = parent

        self.label = ttk.Label(self, text="Event Management")
        self.label.pack()

        self.add_button = ttk.Button(self, text="Add Event", command=self.add_event)
        self.add_button.pack()

        self.delete_button = ttk.Button(self, text="Delete Event", command=self.delete_event)
        self.delete_button.pack()

        self.modify_button = ttk.Button(self, text="Modify Event", command=self.modify_event)
        self.modify_button.pack()

        self.display_button = ttk.Button(self, text="Display Event Details", command=self.display_event_details)
        self.display_button.pack()

    def add_event(self):
        # Implement functionality to add event here
        pass

    def delete_event(self):
        # Implement functionality to delete event here
        pass

    def modify_event(self):
        # Implement functionality to modify event here
        pass

    def display_event_details(self):
        # Implement functionality to display event details here
        pass


class ClientFrame(tk.Frame):
    def __init__(self, parent):
        super().__init__(parent)
        self.parent = parent
        self.clients = []

        self.label = ttk.Label(self, text="Client Management")
        self.label.pack()

        self.add_button = ttk.Button(self, text="Add Client", command=self.add_client)
        self.add_button.pack()

        self.delete_button = ttk.Button(self, text="Delete Client", command=self.delete_client)
        self.delete_button.pack()

        self.modify_button = ttk.Button(self, text="Modify Client", command=self.modify_client)
        self.modify_button.pack()

        self.display_button = ttk.Button(self, text="Display Client Details", command=self.display_client_details)
        self.display_button.pack()

    def add_client(self):
        client_id = simpledialog.askinteger("Client Details", "Enter Client ID:")
        if client_id is not None:
            name = simpledialog.askstring("Client Details", "Enter Name:")
            address = simpledialog.askstring("Client Details", "Enter Address:")
            contact_details = simpledialog.askstring("Client Details", "Enter Contact Details:")
            budget = simpledialog.askinteger("Client Details", "Enter Budget:")

            client = Client(client_id, name, address, contact_details, budget)
            self.clients.append(client)
            messagebox.showinfo("Success", "Client added successfully.")

    def delete_client(self):
        client_id = simpledialog.askinteger("Client ID", "Enter Client ID to delete:")
        if client_id is not None:
            for client in self.clients:
                if client.getClientID() == client_id:
                    self.clients.remove(client)
                    messagebox.showinfo("Success", "Client deleted successfully.")
                    return
            messagebox.showerror("Error", "Client not found.")

    def modify_client(self):
        client_id = simpledialog.askinteger("Client ID", "Enter Client ID to modify:")
        if client_id is not None:
            for client in self.clients:
                if client.getClientID() == client_id:
                    name = simpledialog.askstring("Client Details", "Enter Name:", initialvalue=client.getName())
                    if name is not None:
                        address = simpledialog.askstring("Client Details", "Enter Address:",
                                                         initialvalue=client.getAddress())
                        contact_details = simpledialog.askstring("Client Details", "Enter Contact Details:",
                                                                 initialvalue=client.getContactDetails())
                        budget = simpledialog.askinteger("Client Details", "Enter Budget:",
                                                         initialvalue=client.getBudget())

                        client.setName(name)
                        client.setAddress(address)
                        client.setContactDetails(contact_details)
                        client.setBudget(budget)
                        messagebox.showinfo("Success", "Client modified successfully.")
                        return
            messagebox.showerror("Error", "Client not found.")

    def display_client_details(self):
        client_id = simpledialog.askinteger("Client ID", "Enter Client ID:")
        if client_id is not None:
            for client in self.clients:
                if client.getClientID() == client_id:
                    messagebox.showinfo("Client Details",
                                        f"Client ID: {client.getClientID()}\nName: {client.getName()}\nAddress: {client.getAddress()}\nContact Details: {client.getContactDetails()}\nBudget: {client.getBudget()}")
                    return
            messagebox.showerror("Error", "Client not found.")


class GuestFrame(tk.Frame):
    def __init__(self, parent):
        super().__init__(parent)
        self.parent = parent
        self.guests = []

        self.label = ttk.Label(self, text="Guest Management")
        self.label.pack()

        self.add_button = ttk.Button(self, text="Add Guest", command=self.add_guest)
        self.add_button.pack()

        self.delete_button = ttk.Button(self, text="Delete Guest", command=self.delete_guest)
        self.delete_button.pack()

        self.modify_button = ttk.Button(self, text="Modify Guest", command=self.modify_guest)
        self.modify_button.pack()

        self.display_button = ttk.Button(self, text="Display Guest Details", command=self.display_guest_details)
        self.display_button.pack()

    def add_guest(self):
        guest_id = simpledialog.askinteger("Guest Details", "Enter Guest ID:")
        if guest_id is not None:
            name = simpledialog.askstring("Guest Details", "Enter Name:")
            address = simpledialog.askstring("Guest Details", "Enter Address:")
            contact_details = simpledialog.askstring("Guest Details", "Enter Contact Details:")

            guest = Guest(guest_id, name, address, contact_details)
            self.guests.append(guest)
            messagebox.showinfo("Success", "Guest added successfully.")

    def delete_guest(self):
        guest_id = simpledialog.askinteger("Guest ID", "Enter Guest ID to delete:")
        if guest_id is not None:
            for guest in self.guests:
                if guest.getGuestID() == guest_id:
                    self.guests.remove(guest)
                    messagebox.showinfo("Success", "Guest deleted successfully.")
                    return
            messagebox.showerror("Error", "Guest not found.")

    def modify_guest(self):
        guest_id = simpledialog.askinteger("Guest ID", "Enter Guest ID to modify:")
        if guest_id is not None:
            for guest in self.guests:
                if guest.getGuestID() == guest_id:
                    name = simpledialog.askstring("Guest Details", "Enter Name:", initialvalue=guest.getName())
                    if name is not None:
                        address = simpledialog.askstring("Guest Details", "Enter Address:",
                                                         initialvalue=guest.getAddress())
                        contact_details = simpledialog.askstring("Guest Details", "Enter Contact Details:",
                                                                 initialvalue=guest.getContactDetails())

                        guest.setName(name)
                        guest.setAddress(address)
                        guest.setContactDetails(contact_details)
                        messagebox.showinfo("Success", "Guest modified successfully.")
                        return
            messagebox.showerror("Error", "Guest not found.")

    def display_guest_details(self):
        guest_id = simpledialog.askinteger("Guest ID", "Enter Guest ID:")
        if guest_id is not None:
            for guest in self.guests:
                if guest.getGuestID() == guest_id:
                    messagebox.showinfo("Guest Details",
                                        f"Guest ID: {guest.getGuestID()}\nName: {guest.getName()}\nAddress: {guest.getAddress()}\nContact Details: {guest.getContactDetails()}")
                    return
            messagebox.showerror("Error", "Guest not found.")


class SupplierFrame(tk.Frame):
    def __init__(self, parent):
        super().__init__(parent)
        self.parent = parent
        self.suppliers = []

        self.label = ttk.Label(self, text="Supplier Management")
        self.label.pack()

        self.add_button = ttk.Button(self, text="Add Supplier", command=self.add_supplier)
        self.add_button.pack()

        self.delete_button = ttk.Button(self, text="Delete Supplier", command=self.delete_supplier)
        self.delete_button.pack()

        self.modify_button = ttk.Button(self, text="Modify Supplier", command=self.modify_supplier)
        self.modify_button.pack()

        self.display_button = ttk.Button(self, text="Display Supplier Details", command=self.display_supplier_details)
        self.display_button.pack()

    def add_supplier(self):
        supplier_id = simpledialog.askinteger("Supplier Details", "Enter Supplier ID:")
        if supplier_id is not None:
            name = simpledialog.askstring("Supplier Details", "Enter Name:")
            address = simpledialog.askstring("Supplier Details", "Enter Address:")
            contact_details = simpledialog.askstring("Supplier Details", "Enter Contact Details:")

            supplier = Supplier(supplier_id, name, address, contact_details)
            self.suppliers.append(supplier)
            messagebox.showinfo("Success", "Supplier added successfully.")

    def delete_supplier(self):
        supplier_id = simpledialog.askinteger("Supplier ID", "Enter Supplier ID to delete:")
        if supplier_id is not None:
            for supplier in self.suppliers:
                if supplier.getSupplierID() == supplier_id:
                    self.suppliers.remove(supplier)
                    messagebox.showinfo("Success", "Supplier deleted successfully.")
                    return
            messagebox.showerror("Error", "Supplier not found.")

    def modify_supplier(self):
        supplier_id = simpledialog.askinteger("Supplier ID", "Enter Supplier ID to modify:")
        if supplier_id is not None:
            for supplier in self.suppliers:
                if supplier.getSupplierID() == supplier_id:
                    name = simpledialog.askstring("Supplier Details", "Enter Name:", initialvalue=supplier.getName())
                    if name is not None:
                        address = simpledialog.askstring("Supplier Details", "Enter Address:",
                                                         initialvalue=supplier.getAddress())
                        contact_details = simpledialog.askstring("Supplier Details", "Enter Contact Details:",
                                                                 initialvalue=supplier.getContactDetails())

                        supplier.setName(name)
                        supplier.setAddress(address)
                        supplier.setContactDetails(contact_details)
                        messagebox.showinfo("Success", "Supplier modified successfully.")
                        return
            messagebox.showerror("Error", "Supplier not found.")

    def display_supplier_details(self):
        supplier_id = simpledialog.askinteger("Supplier ID", "Enter Supplier ID:")
        if supplier_id is not None:
            for supplier in self.suppliers:
                if supplier.getSupplierID() == supplier_id:
                    messagebox.showinfo("Supplier Details",
                                        f"Supplier ID: {supplier.getSupplierID()}\nName: {supplier.getName()}\nAddress: {supplier.getAddress()}\nContact Details: {supplier.getContactDetails()}")
                    return
            messagebox.showerror("Error", "Supplier not found.")


class VenueFrame(tk.Frame):
    def __init__(self, parent):
        super().__init__(parent)
        self.parent = parent
        self.venues = []

        self.label = ttk.Label(self, text="Venue Management")
        self.label.pack()

        self.add_button = ttk.Button(self, text="Add Venue", command=self.add_venue)
        self.add_button.pack()

        self.delete_button = ttk.Button(self, text="Delete Venue", command=self.delete_venue)
        self.delete_button.pack()

        self.modify_button = ttk.Button(self, text="Modify Venue", command=self.modify_venue)
        self.modify_button.pack()

        self.display_button = ttk.Button(self, text="Display Venue Details", command=self.display_venue_details)
        self.display_button.pack()

    def add_venue(self):
        venue_id = simpledialog.askinteger("Venue Details", "Enter Venue ID:")
        if venue_id is not None:
            name = simpledialog.askstring("Venue Details", "Enter Name:")
            address = simpledialog.askstring("Venue Details", "Enter Address:")
            contact = simpledialog.askstring("Venue Details", "Enter Contact:")
            min_guests = simpledialog.askinteger("Venue Details", "Enter Min Guests:")
            max_guests = simpledialog.askinteger("Venue Details", "Enter Max Guests:")

            venue = Venue(venue_id, name, address, contact, min_guests, max_guests)
            self.venues.append(venue)
            messagebox.showinfo("Success", "Venue added successfully.")

    def delete_venue(self):
        venue_id = simpledialog.askinteger("Venue ID", "Enter Venue ID to delete:")
        if venue_id is not None:
            for venue in self.venues:
                if venue.getVenueID() == venue_id:
                    self.venues.remove(venue)
                    messagebox.showinfo("Success", "Venue deleted successfully.")
                    return
            messagebox.showerror("Error", "Venue not found.")

    def modify_venue(self):
        venue_id = simpledialog.askinteger("Venue ID", "Enter Venue ID to modify:")
        if venue_id is not None:
            for venue in self.venues:
                if venue.getVenueID() == venue_id:
                    name = simpledialog.askstring("Venue Details", "Enter Name:", initialvalue=venue.getName())
                    if name is not None:
                        address = simpledialog.askstring("Venue Details", "Enter Address:",
                                                         initialvalue=venue.getAddress())
                        contact = simpledialog.askstring("Venue Details", "Enter Contact:",
                                                         initialvalue=venue.getContact())
                        min_guests = simpledialog.askinteger("Venue Details", "Enter Min Guests:",
                                                             initialvalue=venue.getMinGuests())
                        max_guests = simpledialog.askinteger("Venue Details", "Enter Max Guests:",
                                                             initialvalue=venue.getMaxGuests())

                        venue.setName(name)
                        venue.setAddress(address)
                        venue.setContact(contact)
                        venue.setMinGuests(min_guests)
                        venue.setMaxGuests(max_guests)
                        messagebox.showinfo("Success", "Venue modified successfully.")
                        return
            messagebox.showerror("Error", "Venue not found.")

    def display_venue_details(self):
        venue_id = simpledialog.askinteger("Venue ID", "Enter Venue ID:")
        if venue_id is not None:
            for venue in self.venues:
                if venue.getVenueID() == venue_id:
                    messagebox.showinfo("Venue Details",
                                        f"Venue ID: {venue.getVenueID()}\nName: {venue.getName()}\nAddress: {venue.getAddress()}\nContact: {venue.getContact()}\nMin Guests: {venue.getMinGuests()}\nMax Guests: {venue.getMaxGuests()}")
                    return
            messagebox.showerror("Error", "Venue not found.")


if __name__ == "__main__":
    app = EventManagementApp()
    app.mainloop()
