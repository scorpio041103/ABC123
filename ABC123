‎import { useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs";
‎
‎export default function AdminDashboard() { const [loggedIn, setLoggedIn] = useState(false); const [tab, setTab] = useState("users");
‎
‎const dummyUsers = [ { id: 1, name: "UserA", saldo: 50000 }, { id: 2, name: "UserB", saldo: 20000 }, ];
‎
‎const dummyGames = ["Dragon Slot", "Zeus Power", "Panda Gold"];
‎
‎return ( <div className="min-h-screen bg-gray-100 p-4"> {!loggedIn ? ( <Card className="max-w-sm mx-auto mt-20"> <CardContent className="p-4 space-y-4"> <h2 className="text-xl font-bold text-center">Login Admin</h2> <Input placeholder="Username" /> <Input placeholder="Password" type="password" /> <Button onClick={() => setLoggedIn(true)} className="w-full"> Login </Button> </CardContent> </Card> ) : ( <div className="max-w-4xl mx-auto"> <h1 className="text-2xl font-bold mb-4">Dashboard Admin - abc123</h1> <Tabs defaultValue={tab} onValueChange={setTab}> <TabsList> <TabsTrigger value="users">User</TabsTrigger> <TabsTrigger value="games">Permainan</TabsTrigger> <TabsTrigger value="rekening">Rekening Admin</TabsTrigger> </TabsList>
‎
‎<TabsContent value="users" className="mt-4 space-y-4">
‎          {dummyUsers.map((user) => (
‎            <Card key={user.id}>
‎              <CardContent className="flex justify-between items-center p-4">
‎                <div>
‎                  <p className="font-semibold">{user.name}</p>
‎                  <p>Saldo: Rp{user.saldo.toLocaleString()}</p>
‎                </div>
‎                <Button size="sm">Edit Saldo</Button>
‎              </CardContent>
‎            </Card>
‎          ))}
‎        </TabsContent>
‎
‎        <TabsContent value="games" className="mt-4 space-y-4">
‎          {dummyGames.map((game, index) => (
‎            <Card key={index}>
‎              <CardContent className="p-4 flex justify-between items-center">
‎                <p>{game}</p>
‎                <Button size="sm">Edit</Button>
‎              </CardContent>
‎            </Card>
‎          ))}
‎          <Button>+ Tambah Permainan</Button>
‎        </TabsContent>
‎
‎        <TabsContent value="rekening" className="mt-4">
‎          <Card>
‎            <CardContent className="space-y-4 p-4">
‎              <p className="font-semibold">No. Rekening Admin</p>
‎              <Input placeholder="Masukkan nomor rekening" defaultValue="1234567890" />
‎              <Button>Simpan</Button>
‎            </CardContent>
‎          </Card>
‎        </TabsContent>
‎      </Tabs>
‎    </div>
‎  )}
‎</div>
‎
‎); }
‎
‎
