## Bank system workflows

---

# Workflows and Data Requirements

## User Login

**Purpose**: Authenticate a user and login to their account.

**Steps**:

1. Enter username and password on the login page.
2. The system checks the provided credentials against stored data.
3. If the credentials are correct, the user is logged in and redirected to their account dashboard.
4. If the credentials are incorrect, an error message is displayed, and the user is prompted to try again.

**Data Involved**:

- Username
- Password

---

## View Account Balance

**Purpose**: Allow a user to view the current balance of their account.

**Steps**:

1. Navigate to the account balance page.
2. The system fetches the balance for the user’s account from the database.
3. The balance is displayed on the user’s screen.

**Data Involved**:

- User ID
- Account ID
- Current Balance

---

## Money Transfer

**Purpose**: Transfer funds from one account to another.

**Steps**:

1. Enter details for the transfer, including the recipient’s account number, amount, and any notes.
2. The system validates the transfer details, including sufficient balance in the sender’s account.
3. The system processes the transfer by deducting the amount from the sender’s account and crediting it to the recipient’s account.
4. A confirmation message is displayed to the user, and a transaction record is created.

**Data Involved**:

- Sender Account ID
- Recipient Account ID
- Transfer Amount
- Transaction Notes

---

## Update Profile Information

**Purpose**: Allow a user to update their personal information such as name and email address.

**Steps**:

1. Navigate to the profile update page and enter new details.
2. The system checks the validity of the new data (e.g., email format, name validations).
3. The system updates the user’s profile information in the database.

**Data Involved**:

- User ID
- New Name
- New Email Address

---

# Nodes and Edges

## Entities (Nodes)

- **User**
- **Account**
- **Transaction**
- **Profile**
- **PaymentMethod**

---

## Relationships (Edges)

### User → Account

- **Edge**: Each User can have multiple Account instances.
- **Connection**: The User type has a list of Account instances or a field that provides access to the Account type.

---

### Account → Transaction

- **Edge**: Each Account can have multiple Transaction records.
- **Connection**: The Account type has a list of Transaction instances or a field that provides access to the Transaction type.

---

### User → Profile

- **Edge**: Each User has a single Profile.
- **Connection**: The User type includes a field for Profile, linking directly to the Profile type.

---

### User → PaymentMethod

- **Edge**: Each User can have multiple PaymentMethod instances.
- **Connection**: The User type includes a list of PaymentMethod instances or a field for PaymentMethod that links to the PaymentMethod type.

---

### Transaction → Account

- **Edge**: Each Transaction is associated with a specific Account.
- **Connection**: The Transaction type includes a field for Account, linking directly to the Account type.

---

### Profile → User

- **Edge**: Each Profile is linked to a single User.
- **Connection**: The Profile type includes a field for User, linking directly to the User type.

---

Feel free to adjust or expand on any sections as needed!
