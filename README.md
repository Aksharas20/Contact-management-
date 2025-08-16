# Contact-management-const mongoose = require("mongoose");

const contactSchema = new mongoose.Schema({
  name: { type: String, required: true },
  phone: { type: String, required: true },
  email: { type: String },
}, { timestamps: true });

module.exports = mongoose.model("Contact", contactSchema);import { BrowserRouter as Router, Routes, Route } from "react-router-dom";
import ContactList from "./pages/ContactList";
import AddContact from "./pages/AddContact";
import EditContact from "./pages/EditContact";

function App() {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<ContactList />} />
        <Route path="/add" element={<AddContact />} />
        <Route path="/edit/:id" element={<EditContact />} />
      </Routes>
    </Router>
  );
}

export default App;const [search, setSearch] = useState("");
const filteredContacts = contacts.filter(c =>
  c.name.toLowerCase().includes(search.toLowerCase())
);const [search, setSearch] = useState("");
const filteredContacts = contacts.filter(c =>
  c.name.toLowerCase().includes(search.toLowerCase())
);
