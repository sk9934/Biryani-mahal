import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { useState } from "react";

export default function BiryaniMahal() {
  const [email, setEmail] = useState("");

  return (
    <div className="min-h-screen bg-yellow-50 text-gray-800">
      <header className="bg-red-600 text-white p-6 shadow-md">
        <h1 className="text-3xl font-bold">Biryani Mahal - Dalsinghsarai</h1>
        <p className="text-sm mt-1">Authentic Flavours of Biryani in the Heart of Bihar</p>
      </header>

      <section className="p-8 grid gap-6 md:grid-cols-2">
        <Card className="bg-white shadow-lg rounded-2xl p-6">
          <CardContent>
            <h2 className="text-2xl font-semibold mb-4">About Us</h2>
            <p>
              Welcome to Biryani Mahal, Dalsinghsarai's favourite destination for authentic and delicious biryani. We serve a variety of mouth-watering biryanis prepared with the finest ingredients and traditional recipes.
            </p>
          </CardContent>
        </Card>

        <Card className="bg-white shadow-lg rounded-2xl p-6">
          <CardContent>
            <h2 className="text-2xl font-semibold mb-4">Our Specialties</h2>
            <ul className="list-disc pl-5 space-y-1">
              <li>Hyderabadi Chicken Biryani</li>
              <li>Lucknowi Mutton Biryani</li>
              <li>Veg Dum Biryani</li>
              <li>Kebabs & Rolls</li>
              <li>Special Raita and Desserts</li>
            </ul>
          </CardContent>
        </Card>
      </section>

      <section className="p-8 bg-yellow-100">
        <h2 className="text-2xl font-semibold mb-4">Reserve a Table / Order Online</h2>
        <form className="flex flex-col gap-4 md:w-1/2">
          <Input
            type="email"
            placeholder="Enter your email for updates / booking"
            value={email}
            onChange={(e) => setEmail(e.target.value)}
          />
          <Button className="bg-red-600 hover:bg-red-700 text-white">Submit</Button>
        </form>
      </section>

      <footer className="bg-red-600 text-white text-center p-4">
        <p>Biryani Mahal © {new Date().getFullYear()} | Dalsinghsarai, Bihar</p>
      </footer>
    </div>
  );
}
