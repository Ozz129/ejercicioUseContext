# ejercicioUseContext

import React, { createContext } from "react";

export const ThemeContext = createContext();

import React, { useState } from "react";
import { ThemeContext } from "./ThemeContext";

const App = () => {
  const [theme, setTheme] = useState("light");

  return (
  
      {/* ... resto de la aplicación ... */}
      
  );
};

export default App;

# Componentes Hijos

import { ThemeContext } from "./ThemeContext";

const Child = () => {
  const { theme } = useContext(ThemeContext);

  return (
    <div>
      <h2>The theme is {theme}</h2>
      <button onClick={() => setTheme("dark")}>Switch to dark</button>
    </div>
  );
};

export default Child;
